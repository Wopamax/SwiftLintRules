# force_cast
----------

# Why was this rule disabled :
----------
Although force casting is often a bad thing, there are a few places on iOS where
it is commonly used and it is very handy sometimes.  
Most of the time, it is used when casting `UITableViewCell`s subclasses in
`tableView(_:, cellForRowAtIndexPath:)`, and no matter what the app wouldn't behave properly if the cell couldn't be dequeued, since this method excepts a `UITableViewCell` to be returned no matter what.  
Another example is instantiating `UIViewController` subclasses from a `UIStoryboard` instance. If the view controller doesn't match the type it is force-casted too, the app won't behave properly either.

# Examples
----------

```swift
static var appDelegate: AppDelegate {
    return UIApplication.sharedApplication().delegate as! AppDelegate
}
```

```swift
let cell = tableView.dequeueReusableCellWithIdentifier(FavoriteItemTableViewCell.cellReuseIdentifier, forIndexPath: indexPath) as! FavoriteItemTableViewCell
```

```swift
UIStoryboard(name: "iPadLists", bundle: nil).instantiateInitialViewController() as! iPadUserListsViewController
```
