# One Time Work Manager
![image](https://github.com/ArjunGupta08/Work-Manager-OneTime/assets/85922120/bf84d020-f180-444f-bd18-d9ba76275756)
    
        Constraints constraints = new Constraints.Builder()
                .setRequiredNetworkType(NetworkType.CONNECTED)
                .setRequiresBatteryNotLow(true)
                .build();
        OneTimeWorkRequest oneTimeWorkRequest = new OneTimeWorkRequest.Builder(MyWorker.class)
                .setConstraints(constraints)
                .build();
        WorkManager.getInstance(this).enqueue(oneTimeWorkRequest);
