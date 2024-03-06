# One Time Work Manager
![image](https://github.com/ArjunGupta08/Work-Manager-OneTime/assets/85922120/bf84d020-f180-444f-bd18-d9ba76275756)

 - Project SetUp
    
        val workVersion = "2.9.0"
    
        // (Java only)
        implementation("androidx.work:work-runtime:$workVersion")
    
        // Kotlin + coroutines
        implementation("androidx.work:work-runtime-ktx:$workVersion")

 - Create your worker class
 - initialise your one time work request

        Constraints constraints = new Constraints.Builder()
                .setRequiredNetworkType(NetworkType.CONNECTED)
                .setRequiresBatteryNotLow(true)
                .build();
        OneTimeWorkRequest oneTimeWorkRequest = new OneTimeWorkRequest.Builder(MyWorker.class)
                .setConstraints(constraints)
                .build();
        WorkManager.getInstance(this).enqueue(oneTimeWorkRequest);
