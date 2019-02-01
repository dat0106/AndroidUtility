# AndroidUtility (Java) (Kotlin)


This library contain:

1. Logcat
2. Snackbar
3. Toast
4. CollectionUtils
5. AppUtils
6. DateUtils
7. StringUtils
8. FileUtils
9. Shared Preference

# How to integrate:

1. Download and extract folder 
2. Copy utils folder in your folder app->src->main->java->yourpackagename-> <utils>
3. Now ready to use some basics of android applications

=============================================================================
# How to integrate this utility in your application:
=============================================================================
# 1. Logcat

For debug :

DNALog.d("this is debug message");

For error :

DNALog.e("this is debug message");

For info :

DNALog.i("this is debug message");

For verbose :

DNALog.v("this is debug message");


Benifits:
1. It provide support in JAVA as well as KOTLIN
2. This log will work only in debug application.
3. It will give you more information then simple log.

=============================================================================

# 2. Snackbar


DNASnackBar.show( this," this is test message");


Benifits:
1. It provide support in JAVA as well as KOTLIN
2. A single class have multiple function.
3. Handling null pointer
4. if given activity is is null or context then no crash and it will show toast.

=============================================================================

# 3. Toast
// call method
DNAToast.show(this, " this is test message");

Benifits:
1. It provide support in JAVA as well as KOTLIN
2. A single class have multiple function.
3. Handling null pointer

=============================================================================

# 4. CollectionUtils

 List<T> mediaList = new ArrayList();
        if (DNACollectionUtils.isEmpty(mediaList)) {
            // do your stuff 
        }

        if (DNACollectionUtils.isNotEmpty(mediaList)) {
            // do your stuff 
        }
        
   Benifits:
1. It provide support in JAVA as well as KOTLIN
2. It will work for all collections like list, arraylist, hashmap etc
3. Handling null pointer in side method
     
     
=============================================================================

# 5. AppUtils

// provide all details about application at one place.

DNALog.d("App Id"+ DNAAppUtils.getApplicationId());

DNALog.d("App Id"+ DNAAppUtils.getApplicationPackageName());

DNALog.d("Version Code : "+ DNAAppUtils.getAppVersionCode());

DNALog.d("Version Name : "+ DNAAppUtils.getAppVersionName());

DNALog.d("Build Type: "+ DNAAppUtils.getBuildType());

DNALog.d("This is bug build : "+ DNAAppUtils.isBuildType());



 Benifits:
1. It provide support in JAVA as well as KOTLIN
2. It will provide all application information at same place.
3. Easy to integrate and easy to use and provide a support for application
        
=============================================================================



# 5. SharedPreference

In Application file just initialise Preference at once in OnCreate .

      public class UtilityApplication extends Application {

    @Override
    public void onCreate() {
        super.onCreate();


        // java
        DNASharedPreferenceUtils.init(this);
        //or
        //pass custom parameter
        DNASharedPreferenceUtils.init(this, "preference_name", Context.MODE_PRIVATE);



        //kotlin
        datanapps.androidutility.utils.kotlin.DNASharedPreferenceUtils.INSTANCE.init(this);
        //or
        //pass custom parameter
        datanapps.androidutility.utils.kotlin.DNASharedPreferenceUtils.INSTANCE.init(this, "preference_name", Context.MODE_PRIVATE);


    }
}


To use in Application:


        // for save value
        DNASharedPreferenceUtils.saveString("key", "this is my value");

        //get value
        DNALog.d(" value :  "+ DNASharedPreferenceUtils.getString("key"));

 Benifits:
1. It provide support in JAVA as well as KOTLIN
2. It provide all method to save like STRING, FLOAT, INTEGER, LONG, BOOLEAN.
3. Easy to integrate and easy to use and provide.
4. All above repo class is tested.
