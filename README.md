# AndSes6Ass3
MainActivity.java
package me.rk.andses6ass3;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.Menu;
import android.view.MenuItem;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

    private TextView menuTextView;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        menuTextView=(TextView) findViewById(R.id.textView);
    }

    @Override
    public boolean onCreateOptionsMenu(Menu menu) {
        getMenuInflater().inflate(R.menu.menu_activity, menu);
        return true;
    }

    @Override
    public boolean onOptionsItemSelected(MenuItem item) {
        int itemID=item.getItemId();
        menuTextView.setText("SubMenuXmlActivity!");
        switch (itemID){
            case R.id.reditem:
                menuTextView.setTextColor(0xFFFF0000);
                return true;

            case R.id.greenitem:
                menuTextView.setTextColor(0xFF00FF11);
                return true;

            case R.id.blueitem:
                menuTextView.setTextColor(0xFF0004FF);
                return true;
        }


        return super.onOptionsItemSelected(item);
    }
}

activity_main.xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingBottom="@dimen/activity_vertical_margin"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    tools:context="me.rk.andses6ass3.MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:textSize="25dp"
        android:layout_centerInParent="true"
        android:text="Hello World!" />

</RelativeLayout>

menu_activity.xml
<?xml version="1.0" encoding="utf-8"?>
<menu xmlns:android="http://schemas.android.com/apk/res/android">

    <item android:id="@+id/reditem"
        android:title="Red"/>

    <item android:id="@+id/greenitem"
        android:title="Green"/>

    <item android:id="@+id/blueitem"
        android:title="Blue"/>

</menu>
