# jsdatepick
JsDatePick is a pure javascript / jQuery based date picker with a small footprint

## Configuration settings:
	
### useMode (Integer)

* 1 – The calendar's HTML will be directly appended to the field supplied by target
* 2 – The calendar will appear as a popup when the field with the id supplied in target is clicked.
	
### target (String)
The id of the field to attach the calendar to , usually a text input field when using useMode 2.

### isStripped (Boolean)
When set to true the calendar appears without the visual design - usually used with useMode 1

### selectedDate (Object)
When supplied , this object tells the calendar to open up with this date selected already.

### yearsRange (Array)
When supplied , this array sets the limits for the years enabled in the calendar.

### limitToToday (Boolean)
Enables you to limit the possible picking days to today's date.

### cellColorScheme (String)
Enables you to swap the colors of the date's cells from a wide range of colors.
Available color schemes:
 
* torqoise 
* purple 
* pink
* orange
* ocean_blue <-default
* peppermint
* aqua
* armygreen
* bananasplit
* beige
* deepblue
* greenish
* lightgreen

### dateFormat (String)

Enables easy switch of the date format without any hassle 
Should you not supply anything this field will default to: "%m-%d-%Y"

Possible values to use in the date format:

* %d - Day of the month, 2 digits with leading zeros
* %j - Day of the month without leading zeros

* %m - Numeric representation of a month, with leading zeros
* %M - A short textual representation of a month, three letters
* %n - Numeric representation of a month, without leading zeros
* %F - A full textual representation of a month, such as January or March

* %Y - A full numeric representation of a year, 4 digits
* %y - A two digit representation of a year

You can of course put whatever divider you want between them.

### weekStartDay (Integer)
Enables you to change the day that the week starts on.

* Possible values 0 (Sunday) through 6 (Saturday)
* Default value is 1 (Monday)

## Some usage examples

All examples require adding a link to the script and the stylesheet in your HTML document 

The simplest kind of setup to the calendar involve the following code:
```javascript
var calendar = new JsDatePick({
        useMode:2,
        target:"inputField",
        dateFormat:"%d-%M-%Y"
    });
};
```

A more advanced usage scenario:
```javascript
var calendar = new JsDatePick({
    useMode:1,
    isStripped:true,
    target:"div3_example"
    selectedDate:{		
        day:5,
        month:9,
        year:2006
    },
    yearsRange:[1978,2020],
    limitToToday:false,
    cellColorScheme:"beige",
    dateFormat:"%m-%d-%Y",
    imgPath:"img/",
    weekStartDay:1
});
```


Note: We have implemented a way to change the image path of the img folder should you decide you want to move it somewhere else.
Please read through the instructions on how to carefully accomplish that just in the next comment!
	
## License
Copyright 2009-2016 Itamar Arjuan
jsDatePick is distributed under the terms of the GNU General Public License.
JsDatePick makes use of the jQuery library found at http://jquery.com/
	
Thanks for using my calendar !
Itamar :-)

itamar.arjuan@gmail.com