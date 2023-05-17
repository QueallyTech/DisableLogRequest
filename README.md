# DisableLogRequest

**Need Xposed**  
Automatic approve for app to access device logs (Android 13+)  

**How it works**  
it hook `com.android.server.logcat.LogcatManagerService` and call `onAccessApprovedForClient` on every request  
Note: No activity will be started and the timer limit will not be bypassed.  

Logcat TAG: `DisableLogsRequest`  
see: [LogcatManagerService.java](https://cs.android.com/android/platform/superproject/+/master:frameworks/base/services/core/java/com/android/server/logcat/LogcatManagerService.java) and [LogAccessDialogActivity.java](https://cs.android.com/android/platform/superproject/+/master:frameworks/base/core/java/com/android/internal/app/LogAccessDialogActivity.java)
