[![](https://jitpack.io/v/avipars/unit-Of.svg)](https://jitpack.io/#avipars/unit-Of)


This is a Java-only version of https://github.com/digidemic/UnitOf. 
I also set up the build process with gradle, and set it up with Jitpack. 

I plan on only changing some minor things and possibly adding more units. 
Feel free to submit a pull-request with new features


Add it in your root build.gradle at the end of repositories:

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
Step 2. Add the dependency

	dependencies {
	        implementation 'com.github.avipars:unit-Of:0.0.1'
	}
  


This project is used by:

[unitMeasure: offline unit converter app for android](https://www.unitMeasure.xyz) 
