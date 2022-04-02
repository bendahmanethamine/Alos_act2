# Alos Activity 2

## Introduction
This is a simple activity to demonstrate the use of the use of express rest APIs as an assignment for the course Alos.
the project itself is the A prayerTime API.
it is designed to allow for querying of prayer times in a given wilaya and date.
Mocha chai and express validator are used to test the API.

Check Screenshots Folder for Visual.
## Requirements
Node.js

Express

Express-validator

Mocha

Chai

## how to use 

run the server by typing in the terminal:

``` npm start ```

then

```npm install```

then go to the url:

``` http://localhost:3000 ```


## API

list of all the endpoints:

```/prayertime/:wilaya/```
this endpoint will return the prayer times for a given wilaya for all generated times in prayertimeDB.

```/prayertime/:wilaya/:date```
this endpoint will return the prayer times for a given wilaya for a given date.

```/prayertime/:wilaya/:date/:year```
this endpoint will return the prayer times for a given wilaya for a given date and year.

```/prayertime/:wilaya/:date/:year/:month```
this endpoint will return the prayer times for a given wilaya for a given date, year and month.

```/prayertime/:wilaya/:date/:year/:month/:day```
this endpoint will return the prayer times for a given wilaya for a given date, year, month and day.

```/prayertime/:wilaya/:date/:year/:month/:day/:eventname```
this endpoint will return the prayer times for a given Wilaya for a given date, year, month, day and eventname.
valid event-names are:
imsak,fajr,sunrise,dhuhr,asr,sunset,maghrib,isha


## Example

```/prayertime/mostaganem/2022/04/02```
will return 

```
{
[
   {
      "imsak":"05:08",
      "fajr":"05:18",
      "sunrise":"06:45",
      "dhuhr":"13:03",
      "asr":"16:38",
      "sunset":"19:22",
      "maghrib":"19:22",
      "isha":"20:44",
   }
]
}
```

```/prayertime/mostaganem/2022/04/02/magrib```
will return 

```
{
   "maghrib":"19:22"
}
```