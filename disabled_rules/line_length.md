# rule_name
----------

# Why was this rule disabled :
----------
Swift uses Cocoa, which was mostly used with Objective-C and therefore very very
verbose. Most of the delegates/datasources methods are over a 100 chars, and even
splitting those lines don't make the code more readable.

# Examples
----------

```
// 127 chars
func application(application: UIApplication, didFinishLaunchingWithOptions launchOptions: [NSObject: AnyObject]?) -> Bool {
```

```
// 148 chars
func tableView(tableView: UITableView, commitEditingStyle editingStyle: UITableViewCellEditingStyle, forRowAtIndexPath indexPath: NSIndexPath) {
```
