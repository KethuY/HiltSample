// Added the hilt library
// Top-level/Root level build file where you can add configuration options common to all sub-projects/modules.
plugins {
....
id("com.google.dagger.hilt.android") version "2.44" apply false
}

app/build.gradle
plugins {
....
kotlin("kapt")
id("com.google.dagger.hilt.android")
}

dependencies {

.....   
    implementation("com.google.dagger:hilt-android:2.44")
    kapt("com.google.dagger:hilt-android-compiler:2.44")
  .......
}

kapt {
correctErrorTypes = true
}

