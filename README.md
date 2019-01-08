# SingleDateAndTimePicker

You can now select a date and a time with only one widget !


<a href="https://goo.gl/WXW8Dc">
  <img alt="Android app on Google Play" src="https://developer.android.com/images/brand/en_app_rgb_wo_45.png" />
</a>



[![screen](https://raw.githubusercontent.com/florent37/SingleDateAndTimePicker/master/media/new_video.gif)](https://www.github.com/florent37/SingleDateAndTimePicker)

# Usage

```java
new SingleDateAndTimePickerDialog.Builder(context)
            //.bottomSheet()
            //.curved()
            //.minutesStep(15)
            //.displayHours(false)
            //.displayMinutes(false)
            //.todayText("aujourd'hui")
            .displayListener(new SingleDateAndTimePickerDialog.DisplayListener() {
                                @Override
                                public void onDisplayed(SingleDateAndTimePicker picker) {
                                     //retrieve the SingleDateAndTimePicker
                                }
                            })
            
            .title("Simple")
            .listener(new SingleDateAndTimePickerDialog.Listener() {
                @Override
                public void onDateSelected(Date date) {
                    
                }
            }).display();
```

## Display days, months and years

[![screen](https://raw.githubusercontent.com/florent37/SingleDateAndTimePicker/master/media/years_crop.png)](https://www.github.com/florent37/SingleDateAndTimePicker)

```java
new SingleDateAndTimePickerDialog.Builder(this)
            .bottomSheet()
            .curved()
            .displayMinutes(false)
            .displayHours(false)
            .displayDays(false)
            .displayMonth(true)
            .displayYears(true)
            .displayDaysOfMonth(true)
            .display();
```

## Include in a layout

[![screen](https://raw.githubusercontent.com/florent37/SingleDateAndTimePicker/master/media/layout_small.png)](https://www.github.com/florent37/SingleDateAndTimePicker)

```xml
<com.github.florent37.singledateandtimepicker.SingleDateAndTimePicker
        android:layout_width="wrap_content"
        android:layout_height="230dp"
        app:picker_curved="true"
        app:picker_cyclic="true"
        app:picker_visibleItemCount="7"
        />
```

# Customisation

You can change the minutes steps (default : 5min)
```java
new SingleDateAndTimePickerDialog.Builder(context)
            .minutesStep(15)
            .display();
```

And change some colors

[![screen](https://raw.githubusercontent.com/florent37/SingleDateAndTimePicker/master/media/custom_colors.png)](https://www.github.com/florent37/SingleDateAndTimePicker)

```java
new SingleDateAndTimePickerDialog.Builder(context)
            .backgroundColor(Color.BLACK)
            .mainColor(Color.GREEN)
            .titleColor(Color.WHITE)
            .display();
```

# Date range

Force user to select a date between a range

```java
new SingleDateAndTimePickerDialog.Builder(context)
            .defaultDate(defaultDate)
            .minDateRange(minDate)
            .maxDateRange(maxDate)
            .display();
```

Or simply force user to select a future date

```java
new SingleDateAndTimePickerDialog.Builder(context)
            .mustBeOnFuture()
            .display();
```

# Download

[![](https://jitpack.io/v/JYLEE1988/SingleDateAndTimePicker.svg)](https://jitpack.io/#JYLEE1988/SingleDateAndTimePicker)
```groovy	       
implementation 'com.github.JYLEE1988:SingleDateAndTimePicker:(last version)'
```


License
--------

    Copyright 2016 florent37, Inc.

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
