# <p align="center"> Ex.No-4 Design an android application Send SMS using Intent</P>

## AIM:

To create and design an android application Send SMS using Intent using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “ex.no.4″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Send SMS and Display details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to create and design an android application Send SMS using Intent.
Developed by: Gowri M
Registeration Number : 212220230019
*/
```

### MainActivity.java
```java
package com.example.exno4;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        Button mButton= (Button) findViewById(R.id.send_sms);
        mButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent=new Intent(Intent.ACTION_VIEW, Uri.fromParts("sms",
                "9994934716",null));
                intent.putExtra("sms_body","SMS using Intent");
                startActivity(intent);
            }
        });
    }
}
```

### Activity_main.xml
```java
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingLeft="16dp"
    android:paddingRight="16dp"
    android:paddingBottom="16dp"
    android:paddingTop="16dp"
    tools:context=".MainActivity">

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/send_sms"
        android:text="@string/click_here_to_send_sms"/>

</RelativeLayout>
```
</br>
</br>
</br>

## OUTPUT:
![O1 (2)](https://user-images.githubusercontent.com/77089743/167108866-a0a74547-5cb7-4e2b-852d-8a1ad2053580.jpeg)

</br>
</br>
</br>

![O2 (2)](https://user-images.githubusercontent.com/77089743/167108885-1857eaa9-d79f-4c54-bf95-84b80ad0cfb7.jpeg)

## RESULT
Thus a Simple Android Application create and design an android application Send SMS using Intent using Android Studio is developed and executed successfully.
