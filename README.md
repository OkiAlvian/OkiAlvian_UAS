# OkiAlvian_UAS
<appwidget-provider xmlns:android="http://schemas.android.com/apk/res/android" android:minWidth="250dp" android:minHeight="50dp" android:updatePeriodMillis="90000000" android:initialLayout="@layout/appwidget" android:resizeMode="horizontal|vertical" android:widgetCategory="home_screen"> </appwidget-provider>
<resources>
<string name="app_name">androidWidgetPoc</string>
<resources>
<resources>
<dimen name="widget_margin">0dp</dimen>
</resources>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android" android:layout_width="match_parent" android:layout_height="75dp" android:orientation="horizontal" android:id="@+id/widgetItemContainer" android:background="@drawable/rounded_corner_content">
<LinearLayout android:id="@+id/container" android:layout_width="match_parent" android:layout_height="match_parent" android:layout_alignParentLeft="true" android:layout_marginLeft="0dp" android:layout_marginTop="5dp" android:orientation="horizontal">
<ImageView android:id="@+id/ch" android:layout_width="50dp" android:layout_height="50dp" android:layout_alignParentLeft="true" android:layout_marginLeft="5dip" android:layout_marginTop="5dip" android:layout_marginBottom="5dip" android:src="@drawable/jo"/>
</LinearLayout>
<TextView android:id="@+id/heading" android:layout_width="wrap_content" android:layout_height="wrap_content" android:layout_marginTop="5dip" android:layout_marginLeft="65dip" android:singleLine="true" android:textSize="14sp" android:textStyle="bold" android:textColor="#ffffff" android:text="Heading"/>
<TextView android:id="@+id/content" android:layout_width="wrap_content" android:layout_height="40dip" android:layout_below="@id/heading" android:layout_marginTop="5dip" android:layout_marginLeft="65dip" android:layout_marginRight="5dip" android:padding="5dip" android:textSize="14sp" android:textColor="#ffffff" android:background="@drawable/rounded_corner" android:text="Content"/>
</RelativeLayout>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android" xmlns:app="http://schemas.android.com/apk/lib/com.androidwidgetpoc" android:layout_width="match_parent" android:layout_height="match_parent" android:orientation="vertical" android:background="#00000000">
<TextView android:id="@+id/title" android:layout_width="match_parent" android:layout_height="wrap_content" android:text="Hero" android:textStyle="bold" android:textColor="#ffffff" android:background="@drawable/rounded_corner" android:paddingLeft="10dp" android:layout_marginBottom="5dp" android:textSize="21sp"/>
<ListView android:id="@+id/listViewWidget" android:layout_width="match_parent" android:layout_height="match_parent"/>
<LinearLayout android:id="@+id/charms_layout" android:layout_width="match_parent" android:layout_height="wrap_content" android:baselineAligned="false" android:gravity="center_horizontal" android:orientation="vertical"/>
<TextView android:id="@+id/empty_view" android:layout_width="match_parent" android:layout_height="match_parent" android:textColor="#FCFCFC" android:gravity="center" android:background="@drawable/rounded_corner_content" android:text="Nessun elemento."/>
</LinearLayout>
<shape ></shape>xmlns:android="http://schemas.android.com/apk/res/android">
<stroke android:width="1dp" android:color="#4382f5"/>
<solid android:color="#894382f5"/>
<padding android:left="1dp" android:right="1dp" android:top="1dp"/>
<corners android:radius="5dp"/>
</shape>
<shape ></shape>xmlns:android="http://schemas.android.com/apk/res/android">
<stroke android:width="1dp" android:color="#55000000"/>
<solid android:color="#55000000"/>
<padding android:left="1dp" android:right="1dp" android:top="1dp"/>
<corners android:radius="5dp"/>
</shape>
<shape xmlns:android="http://schemas.android.com/apk/res/android">
<solid android:color="#80000000"/>
<corners android:radius="6dp"/>
</shape>
<manifest ></manifest>xmlns:android="http://schemas.android.com/apk/res/android" package="com.androidwidgetpoc" android:versionCode="1" android:versionName="1.0">
<uses-permission android:name="android.permission.INTERNET"/>
<uses-permission android:name="android.permission.SYSTEM_ALERT_WINDOW"/>
<uses-permission android:name="android.permission.WAKE_LOCK"/>
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"/>
<uses-sdk android:minSdkVersion="16" android:targetSdkVersion="22"/>
<application android:name=".MainApplication" android:allowBackup="true" android:label="@string/app_name" android:icon="@mipmap/ic_launcher" android:theme="@style/AppTheme">
<activity android:name=".MainActivity" android:label="@string/app_name" android:configChanges="keyboard|keyboardHidden|orientation|screenSize" android:windowSoftInputMode="adjustResize">
<intent-filter>
<action android:name="android.intent.action.MAIN"/>
<category android:name="android.intent.category.LAUNCHER"/>
</intent-filter>
</activity>
<activity android:name="com.facebook.react.devsupport.DevSettingsActivity"/>
<activity android:name=".CustomReactActivity" android:configChanges="keyboard|keyboardHidden|orientation|screenSize" android:label="@string/app_name" android:windowSoftInputMode="adjustResize">
<intent-filter>
<category android:name="android.intent.category.DEFAULT"/>
</intent-filter>
</activity>
<receiver android:name="WidgetProvider">
<intent-filter>
<action android:name="android.appwidget.action.APPWIDGET_UPDATE"/>
</intent-filter>
<meta-data android:name="android.appwidget.provider" android:resource="@xml/widgetprovider"/>
</receiver>
<service android:name=".BackgroundTask" android:enabled="true" android:label="BackgroundAdd"/>
<service android:name=".WidgetService" android:permission="android.permission.BIND_REMOTEVIEWS"/>
</application>
</manifest>
