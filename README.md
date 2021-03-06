

## How to use ###

### 1) Install using npm ###

```
    npm i ion-datepicker-3 --save
```

### 2) Add it to your ngModule in app.module ###

```
 import { DatePickerModule } from 'ion-datepicker-3';
```
```
   imports: [
        IonicModule.forRoot(App),
        DatePickerModule,
    ],
```
### 3) Use the directive ion-datepicker in your html  ###
```
	<span ion-datepicker (ionChanged)="setDate($event);" [value]="localDate" [min]="localDate" clear class="ScheduleDate">
		<span>{{localDate | date}} <ion-icon name="clipboard" item-left ></ion-icon> </span>
	</span>
```

### Dismiss the datepicker from the class  ###

```

    import { DatePickerDirective } from 'ion-datepicker-3';

	@ViewChild(DatePickerDirective) private datepickerDirective:DatePickerDirective;

    public closeDatepicker(){
        this.datepickerDirective.dismiss();
    }
    
```

## Please note en-US locale starts the calendar with monday and en-UK starts it with sunday ###


 `[value]` - defines the initial value. (not required)

 `[min]` - minimum date that user is allowed to select.  (not required)

 `[max]` - maximum date that user is allowed to select.  (not required)

 `[disabledDates]` - An array of dates that should be disabled (not required)

 `[markDates]` - An array of dates that should be mark (background-color) (not required)

 `(ionChanged)` - an event emitter that returns the date as a $event.

 `(ionCanceled)` - an event that is raised when the cancel button is activated. Returns no data.

 `[headerClasses]` - a bridge to the header classes of the directive using ngClass (string, array or object)  (not required)

 `[bodyClasses]` - a bridge to the date classes of the directive using ngClass (string, array or object)  (not required)

 `[modalOptions]` - a modal is used to display the picker to configure the animation or other options you may use this

 `[locale]` - for translating the calendar. Avaliable local is en-US, en-UK, he-IL, pt-BR, ru-RU, de, fi, zh-TW, zh-CN, it-IT

 `[localeStrings]` - if you dont want to use the built translations - accepts an object { weekdays: string[], months: string[], monday:boolean },
For example: 
            ```
            {
                monday:true,
                weekdays: ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday'],
                months: ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December']
            },
            ```

 `[okText]` - text for the ok button

 `[cancelText]` - text for the cancel button


### 4) Pictures ###

<img src="https://i.gyazo.com/0caf3169c08777da99bf98ba7f328c41.png" height="450">