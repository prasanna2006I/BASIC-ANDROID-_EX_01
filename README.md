# BASIC-ANDROID-_EX_01
## Ex.No:1 Implementation of a Hello world Activity using all lifecycles methods using Android Studio.
## AIM:
To create Hello world Activity using all lifecycles methods to display messages using android studio.

## EQUIPMENTS REQUIRED:
Android Studio(Min. required Artic Fox)

## ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
Program to implement a Hello world Activity using all lifecycles methods using Android Studio .
Developed by: MEENAKSHI.R
RegisterNumber: 212224220062
```
## MainActivity.java:
```
package com.example.andriodlifecycle;

import android.os.Bundle;
import android.widget.Toast;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        EdgeToEdge.enable(this);
        setContentView(R.layout.activity_main);
        Toast toast= Toast.makeText(getApplicationContext(),"OnCreated Executed",Toast.LENGTH_LONG);
        toast.show();
        ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main), (v, insets) -> {
            Insets systemBars = insets.getInsets(WindowInsetsCompat.Type.systemBars());
            v.setPadding(systemBars.left, systemBars.top, systemBars.right, systemBars.bottom);
            return insets;
        });
    }

    protected void onStart(){
        super.onStart();
        Toast toast= Toast.makeText(getApplicationContext(),"OnStart Executed",Toast.LENGTH_LONG);
        toast.show();
    }

    protected void onResume(){
        super.onResume();
        Toast toast= Toast.makeText(getApplicationContext(),"OnResume Executed",Toast.LENGTH_LONG);
        toast.show();
    }

    protected void onPause(){
        super.onPause();
        Toast toast= Toast.makeText(getApplicationContext(),"onPause Executed",Toast.LENGTH_LONG);
        toast.show();
    }

    protected void onStop(){
        super.onStop();
        Toast toast= Toast.makeText(getApplicationContext(),"onStop Executed",Toast.LENGTH_LONG);
        toast.show();
    }

    protected void onRestart(){
        super.onRestart();
        Toast toast= Toast.makeText(getApplicationContext(),"onRestart Executed",Toast.LENGTH_LONG);
        toast.show();
    }

    protected void onDestroy(){
        super.onDestroy();
        Toast toast= Toast.makeText(getApplicationContext(),"onDestroy Executed",Toast.LENGTH_LONG);
        toast.show();
    }
}
```
## activitymain.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Welcome to Andriod LifeCycle"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
## OUTPUT:

## OnCreate Executed:
<img width="148" height="332" alt="366549803-f1dce3e2-64f0-4100-92fa-795d2a88ea77" src="https://github.com/user-attachments/assets/17e94980-8f3d-4bdf-b668-8ba2f540c6bc" />

## OnPause Executed:
<img width="153" height="334" alt="366550076-5ad3ce94-bd9c-4049-9755-be00b59b8849" src="https://github.com/user-attachments/assets/3ea3656d-c839-44c0-9e53-a40292f4861e" />

## OnResume Executed:
<img width="151" height="334" alt="366550236-927b122c-922d-4568-9669-60a329d01659" src="https://github.com/user-attachments/assets/6abe4c1e-f828-45f0-886c-d98871aad7a8" />

## OnRestart Executed:
<img width="150" height="331" alt="366550380-a351f593-8b09-4213-af9e-f9ee173cf8bd" src="https://github.com/user-attachments/assets/e863e797-b9f9-4554-87e7-431318ea2b2a" />

## OnStart Executed:
<img width="150" height="331" alt="366550512-a840e3e9-8745-4c93-adcb-062f92c28e09" src="https://github.com/user-attachments/assets/261015bb-9c9d-43d8-b6dc-86548d0814c5" />

## RESULT:
Thus a program to implement the various life cycles of an activity is written and successfully executed using Android Studio.
