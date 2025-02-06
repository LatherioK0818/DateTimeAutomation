# UiPath Date and Time Tutorial

## Overview
This tutorial covers working with Date and Time functionalities in UiPath, helping users manipulate, format, and perform operations on date and time values within UiPath workflows.

## Prerequisites
- UiPath Studio installed
- Basic knowledge of UiPath workflows and activities

## Topics Covered
1. **Getting Current Date and Time**
2. **Formatting Date and Time**
3. **Adding and Subtracting Time**
4. **Comparing Dates**
5. **Converting Strings to DateTime Objects**
6. **Extracting Date Components**
7. **Handling Time Zones**

## Getting Started
### 1. Getting Current Date and Time
To get the current date and time, use:
```vb
Now
```
Example:
```vb
currentDateTime = Now
```

### 2. Formatting Date and Time
To format the date and time, use the `.ToString()` method:
```vb
Now.ToString("yyyy-MM-dd HH:mm:ss")
```
Other formats:
- `"MM/dd/yyyy"` → 02/06/2025
- `"dddd, MMMM dd, yyyy"` → Thursday, February 06, 2025

### 3. Adding and Subtracting Time
Add or subtract time using `AddDays`, `AddMonths`, `AddYears`, etc.:
```vb
Now.AddDays(5) ' Adds 5 days
Now.AddHours(-3) ' Subtracts 3 hours
```

### 4. Comparing Dates
To compare two dates:
```vb
If date1 > date2 Then
    ' date1 is later than date2
End If
```

### 5. Converting Strings to DateTime Objects
Use `DateTime.Parse` or `DateTime.ParseExact`:
```vb
dateObj = DateTime.Parse("02/06/2025")
```
For custom formats:
```vb
dateObj = DateTime.ParseExact("06-Feb-2025", "dd-MMM-yyyy", System.Globalization.CultureInfo.InvariantCulture)
```

### 6. Extracting Date Components
```vb
day = Now.Day
month = Now.Month
year = Now.Year
hour = Now.Hour
minute = Now.Minute
```

### 7. Handling Time Zones
To convert to a different time zone:
```vb
timeZone = TimeZoneInfo.FindSystemTimeZoneById("Pacific Standard Time")
utcNow = DateTime.UtcNow
pstTime = TimeZoneInfo.ConvertTimeFromUtc(utcNow, timeZone)
```

## Additional Resources
- [UiPath Official Documentation](https://docs.uipath.com/)
- [Microsoft .NET DateTime Documentation](https://learn.microsoft.com/en-us/dotnet/api/system.datetime)

## Conclusion
This tutorial provides a fundamental understanding of date and time operations in UiPath. You can leverage these techniques to automate time-based tasks efficiently.


