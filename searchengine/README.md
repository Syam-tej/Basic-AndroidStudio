# Ex.No:6 Build a program to create a first display screen of any search engine using Auto Complete Text View.

## AIM:

To develop a program to create a first display screen of any search engine using AutoComplete TextView in Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min.required Artic Fox)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as searchengine and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout using AutoComplete TextView in activity_main.xml.

Step 6: Display screen of search engine in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
Program to print the text “display screen of any search engine”.
Developed by:P SYAM TEJ
Registeration Number :212221240056
```
## MainActivity.java:
```
package com.example.auto_complete_view_experiment;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.widget.ArrayAdapter;
import android.widget.AutoCompleteTextView;

public class MainActivity extends AppCompatActivity {
    AutoCompleteTextView autocomplete;

    String[] arr = { "Bing","Google","Yandex","Yahoo","DuckDuckGo","Swisscows","StartPage","Gibiru"};

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        autocomplete = (AutoCompleteTextView)
                findViewById(R.id.autoCompleteTextView1);

        ArrayAdapter<String> adapter = new ArrayAdapter<String>
                (this,android.R.layout.select_dialog_item, arr);

        autocomplete.setThreshold(2);
        autocomplete.setAdapter(adapter);
    }
}
```
### activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#A86D6D"
    android:padding="5dp"
    tools:context=".MainActivity">


    <AutoCompleteTextView
        android:id="@+id/autoCompleteTextView1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@+id/textView2"
        android:layout_centerHorizontal="true"
        android:layout_marginStart="30dp"
        android:layout_marginTop="30dp"
        android:layout_marginEnd="30dp"
        android:layout_marginBottom="30dp"
        android:ems="10"
        android:hint="@string/example_autocompletetextview"
        android:textAlignment="center"
        tools:ignore="UnknownId" />

</RelativeLayout>
```
## OUTPUT

![6 1](https://user-images.githubusercontent.com/93427224/199949896-cb976a71-f043-464a-adbf-7e3ad4ed0b35.jpeg)

![6 2](https://user-images.githubusercontent.com/93427224/199949924-2c017266-43ca-481b-b6d3-8501f7ba8836.jpeg)

![6 3](https://user-images.githubusercontent.com/93427224/199949982-887de555-df06-4d06-8c9e-78794171b386.jpeg)

![6 4](https://user-images.githubusercontent.com/93427224/199950015-8c21b8e8-5145-4469-91d6-a4897f3955bd.jpeg)



## RESULT
Thus a Simple Android Application develop a program to create a first display screen of any search engine using AutoComplete TextView in Android Studio is developed and executed successfully.
