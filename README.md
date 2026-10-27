# Ex.No:2b To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## AIM:

To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

    1. Start the application.
    2. Click the Next button on the main activity.
    3. Create an explicit intent specifying SecondActivity.
    4. Start the intent to open the second activity.
    5. Click the Home button on the second activity.
    6. Create an intent to return to MainActivity.
    7. Start the intent to return to the main activity.


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
<img width="943" height="797" alt="image" src="https://github.com/user-attachments/assets/0b067c29-35c0-4baf-954e-dd0e4c4a6dae" />

<img width="187" height="416" alt="image" src="https://github.com/user-attachments/assets/7868fe48-35f4-43c9-b966-861da2d586bd" />
<img width="187" height="415" alt="image" src="https://github.com/user-attachments/assets/4d2152f6-60ed-4d7f-9ee4-70eff0e15c8e" />



## RESULT
Thus a Simple Android Application create a Explicit Intents using Android Studio is developed and executed successfully.


