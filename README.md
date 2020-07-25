[![](https://jitpack.io/v/avipars/unit-Of.svg)](https://jitpack.io/#avipars/unit-Of)


This is a Java-only version of https://github.com/digidemic/UnitOf. 
I also set up the build process with gradle, and set it up with Jitpack. 

I plan on only changing some minor things and possibly adding more units. 
Feel free to submit a pull-request with new features

This library is used by:

- [unitMeasure: offline unit converter app for android](https://www.unitMeasure.xyz) 

## Table of Contents
- [Examples](#examples)
- [Installation](#installation)
- [Migration](#migration)

## Examples
- https://digidemic.github.io/UnitOf/ provides full documentation of all measurements and units, live examples, FAQ, and much more.
<br><br>

```
//One Liner
double a = new UnitOf.Mass().fromPounds(5).toKilograms(); //2.26796 returned as 5 pounds is 2.26796 kilograms

//Set Then Convert
UnitOf.Length feet = new UnitOf.Length().fromFeet(5.5); //Instantiate UnitOf.Length and set "feet" as 5.5
double b = feet.toInches(); //66 returned as 5.5 feet is 66 inches
double c = feet.toMeters(); //1.6764 returned as 5.5 feet is 1.6764 meters

//Convert Data Type and Fractions
double d = new UnitOf.DataType("12.5").toDouble(); //12.5 of type double returned. 0.0 would be returned if conversion failed
int e = new UnitOf.DataType("Not A Number").toInt(10); //10 of type int returned since conversion fails
String f = new UnitOf.DataType(0.5).toFraction(); //"1/2" of type String returned. Empty string would be returned if failed

//Create Your Own Custom Measurement
UnitOf.Anything x = new UnitOf.Anything("FEET", new HashMap<Object, Double>() {{ put("METERS", 0.3048); put("INCHES", 12.0); }});
double g = x.convertNow(36, "INCHES", "FEET"); //3 returned as 36 inches is 3 feet
double h = x.convertNow(3, "FEET", "METERS"); //0.9144 returned as 3 feet is 0.9144 meters
```

---

<br>

## Installation
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
	
## Migration
If you are migrating from the original library, note that the version numbers will not be synced up. 
0.0.1 is based on the 1.0.0.1 build (Latest as of July 25th, 2020). You should delete the libs directory along with the JAR. 
Next, you'll have to remove this input 

       import com.digidemic.unitof.UnitOf;
       
       //in favor of
       import com.aviparshan.unitOf.UnitOf;
      
