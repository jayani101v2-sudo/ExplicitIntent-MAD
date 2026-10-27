# Ex.No:4 To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## AIM:

To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:
```
/*
Program to print the text “ExplicitIntent”.
Developed by: JAYANI N
Registeration Number : 212224100025
*/


## activity_main.xml

<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="24dp">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Welcome to Second Screen!"
        android:textSize="24sp"
        android:textStyle="bold"
        android:layout_marginBottom="24dp" />

    <Button
        android:id="@+id/homeButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Go Back to Home" />

</LinearLayout>



## MainActivity.java

package com.example.intents;

import android.content.Intent;
import android.os.Bundle;
import android.widget.Button;

import androidx.appcompat.app.AppCompatActivity;

public class SecondActivity extends AppCompatActivity {

    Button homeButton;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_second);

        homeButton = findViewById(R.id.homeButton);

        // Explicit Intent: Return to MainActivity
        homeButton.setOnClickListener(v -> {

            Intent intent = new Intent(
                    SecondActivity.this,
                    MainActivity.class
            );

            startActivity(intent);
            finish();
        });
    }
}


```

## OUTPUT

<img width="1040" height="941" alt="image" src="https://github.com/user-attachments/assets/0b9bb697-821e-4652-91ba-e0cf133a923a" />



## RESULT
Thus a Simple Android Application create a Explicit Intents using Android Studio is developed and executed successfully.


