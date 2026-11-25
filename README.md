
# Ex.No: 7 Design an application that draws basic graphical primitives on the screen.

## DATE : 25.11.2026

## AIM:

To create and design an android application that draws basic graphical primitives on the screen using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “graphical″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Draw basic object details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:

/*
Program to create and design an android application that draws basic graphical primitives on the screen.

Developed by: JENOVIYA D

Registeration Number : 212225040151
*/

## ACTIVITY_MAIN.XML :

~~~
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:background="#D3D3D3">

    <!-- Space for Camera -->
    <View
        android:layout_width="match_parent"
        android:layout_height="55dp"/>

    <!-- Experiment Topic -->
    <TextView
        android:id="@+id/topicText"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Basic Graphical Primitives"
        android:textSize="20sp"
        android:textStyle="bold"
        android:textColor="#000000"
        android:gravity="center"
        android:padding="12dp"
        android:background="#D3D3D3"/>

    <!-- Graphics Output -->
    <ImageView
        android:id="@+id/graphicsView"
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:scaleType="fitCenter"
        android:contentDescription="Graphics Output"/>

</LinearLayout>


~~~

## MAINACTIVITY.JAVA :

~~~
package com.example.graphics;

import android.os.Bundle;
import android.graphics.Bitmap;
import android.graphics.Canvas;
import android.graphics.Paint;
import android.graphics.Color;
import android.graphics.LinearGradient;
import android.graphics.Shader;
import android.widget.ImageView;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    ImageView graphicsView;
    Bitmap bitmap;
    Canvas canvas;
    Paint paint;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        graphicsView = findViewById(R.id.graphicsView);

        bitmap = Bitmap.createBitmap(
                800, 1200, Bitmap.Config.ARGB_8888);

        canvas = new Canvas(bitmap);
        paint = new Paint(Paint.ANTI_ALIAS_FLAG);

        // Background Color
        canvas.drawColor(Color.LTGRAY);

        // Text Style
        paint.setTextSize(55);
        paint.setColor(Color.BLACK);
        paint.setStyle(Paint.Style.FILL);

        // Circle Label
        canvas.drawText("Circle", 160, 100, paint);

        // Rectangle Label
        canvas.drawText("Rectangle", 450, 100, paint);

        // Square Label
        canvas.drawText("Square", 160, 650, paint);

        // Line Label
        canvas.drawText("Line", 540, 650, paint);

        // Circle - Blue to Cyan Gradient
        paint.setShader(new LinearGradient(
                100, 150, 400, 150,
                Color.BLUE,
                Color.CYAN,
                Shader.TileMode.CLAMP));

        canvas.drawOval(80, 150, 400, 520, paint);

        paint.setShader(null);

        // Rectangle - Black
        paint.setColor(Color.BLACK);
        paint.setStyle(Paint.Style.FILL);

        canvas.drawRect(450, 150, 700, 600, paint);

        // Square - Purple
        paint.setColor(Color.rgb(128, 0, 128));
        paint.setStyle(Paint.Style.FILL);

        canvas.drawRect(80, 700, 400, 1050, paint);

        // Line - Black
        paint.setColor(Color.BLACK);
        paint.setStrokeWidth(10);
        paint.setStyle(Paint.Style.STROKE);

        canvas.drawLine(550, 700, 550, 1050, paint);

        // Display Output
        graphicsView.setImageBitmap(bitmap);
    }
}

~~~

## OUTPUT : 

## ACTIVITY_MAIN.XML :

<img width="1917" height="1078" alt="Screenshot 2026-11-25 105110" src="https://github.com/user-attachments/assets/57937fdb-2e53-487b-8cb0-15d2a0cac159" />


## MAINACTIVITY.JAVA :

<img width="1917" height="1078" alt="Screenshot 2026-11-25 105055" src="https://github.com/user-attachments/assets/01e1ef17-c906-4b3d-a0cf-12644bc00a62" />




## RESULT
Thus a Simple Android Application to create and design an android application that draws basic graphical primitives on the screen using Android Studio is developed and executed successfully.
