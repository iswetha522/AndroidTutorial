#VIEWS

##TEXTVIEW:													


```xml
<TextView
android:text="Hello Swetha"
android:layout_height="100dp"/>
```

  dp:density independent pixel
  sp:scale independent pixel
  textSize or textAppearance can be small,medium or large


```xml																							
<TextView																					 
android:text="hi this is vijayalakshmi. i hail from vizag"
android:layout_height="wrap_content"
android:layout_width="wrap_content"
android:textSize="45sp"/>
```

or


```xml
<TextView																					 
android:text="hi this is vijayalakshmi. i hail from vizag"
android:background:"@android:color/darker_gray"
android:layout_height="wrap_content"
android:layout_width="wrap_content"
android:textAppearance="?android:textAppearanceLarge"/>
```

in android text colors are limited so we can't access many colors for that reason we are using a new technique


```xml
android:background:"@android:color/darker_gray"
```
or
```xml
android:background="#2196F3"(blue color)
android:textColor="#AED581"(green color text on blue background)
```

##IMAGEVIEW

```xml
<ImageView
android:src="@drawable/cake"
android:layout_height="wrap_content"
android:layout_width="wrap_content"
android:scaleType="centerCrop"/>
```

"drawable" is the name of the folder and "cake" is the image stored in drawable folder. we need not have to mention the extension of the image i.e;jpg or png or jpeg etc;"@" refers to "resource" and "drawable" refers to "resource name or resource type" 
"centerCrop" means we are fitting the image to edge to edge without breaking the image i.e; any kind of large image can't fit due to its larger size but we are adjusting its dimensions and fixing through the screen size.

#XML ATTRIBUTES

##TEXT ALL CAPS

```xml
<TextView
android:text="hi this is vijayalakshmi"
android:layout_height="wrap_content"					/* HI THIS IS VIJAYALAKSHMI */
android:layout_width="wrap_content"
android:textAllCaps="true"/>
<TextView
android:text="hi this is vijayalakshmi"
android:layout_height="wrap_content"					/* hi this is vijayalakshmi */
android:layout_width="wrap_content"
android:textAllCaps="false"/>
```

##TEXT STYLE

```xml
<TextView
android:text="swetha"
android:layout_height="wrap_content"
android:layout_width="wrap_content"
android:textStyle="bold"/>
```

#LINEAR LAYOUT

```xml
<LinearLayout
xmlns:android="http://schemas.android.com/apk/res/android"
android:orientation="vertical"
android:layout_height="wrap_content"
android:layout_width="wrap_content">

<TextView
android:text="Guest List"
android:layout_height="wrap_content"
android:layout_width="wrap_content"/>

<TextView
android:text="Kunal"
android:layout_height="wrap_content"
android:layout_width="wrap_content"/>
</LinearLayout>
```

```xml
<LinearLayout
xmlns:android="http://schemas.android.com/apk/res/android"
android:orientation="vertical"
android:layout_height="match_parent"
android:layout_width="match_parent"
android:background="@android:color/darker/gray">

<TextView
android:text="Guest List"
android:layout_height="match_parent"
android:layout_width="wrap_content"
android:background="#4CAF50"
android:textSize="24sp" />

<TextView
android:text="swetha"
android:layout_height="1000dp"
android:layout_width="50dp"
android:background="#4CAF50"
android:textSize="24sp" />

<TextView
android:text="sowmya"
android:layout_height="400dp"
android:layout_width="wrap_content"
android:background="#4CAF50"
android:textSize="24sp" />

</Linearlayout>
```

##LINEAR WEIGHT

```xml
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:layout_weight="1">

    <TextView
        android:text="Tom"
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:background="#673AB7"
        android:textSize="24sp" />

    <TextView
        android:text="Tim"
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:background:"#2196F3"
        android:textSize="24sp" />

    <TextView
        android:text="Todd"
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:background="#4CAF50"
        android:textSize="24sp" />

</LinearLayout>
```

```xml
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <ImageView
        android:src="@drawable/ocean"
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:scaleType="centerCrop" />

    <TextView
        android:text="You're invited!"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="0"
        android:textColor="@android:color/white"
        android:textSize="54sp"
        android:background="#009688" />

    <TextView
        android:text="Bonfire at the beach"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="0"
        android:textColor="@android:color/white"
        android:textSize="34sp"
        android:background="#009688" />

</LinearLayout>
```

#RELATIVE LAYOUT

##RELATIVE LAYOUT  TO PARENTS

```xml
<RelativeLayout
xmlns:android="http://schemas.android.com/apk/ress/android"
android:layout_width="match_parent"
android:layout_height="match_parent"
android:padding="16dp">


<TextView
android:text="I'm in this corner"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_alignParentBottom="true"
android:layout_alignParentLeft="true" />

<TextView
android:text="No,up here"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_alignParentTop="true"
android:layout_alignParentLeft="true" />

<TextView
android:text="Wait,I'm here"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_alignParentBottom="true"
android:layout_alignParentRight="true" />

<TextView
android:text="Actually,I'm here"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_alignParentTop="true"
android:layout_alignParentRight="true" />

</RelativeLayout>
```

##RELATIVE LAYOUT TO OTHER VIEWS

```xml
<RelativeLayout
xmlns:android="http://schemaas.android.com/apk/res/android"
android:layout_width="match_parent"
android:layout_height="match_parent">

<TextView
android:id="@+id/ben_text_view"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_alignParentTop="true"
android:layout_centerHorizontal="true"
android:text="BEN"
android:textSize="24sp" />
 
<TextView
android:id="@+id/kunal_text_view"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_alignParentTop="true"
android:layout_toLeftOf="@id/ben_text_view"
android:text="KUNAL"
android:textSize="24sp" />

<TextView
android:id="@+id/kagure_text_view"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_alignParentTop="true"
android:layout_toRightOf="@id/ben_text_view"
android:text="KAGURE"
android:textSize="24sp" />

<TextView
android:id="@+id/lyla_text_view"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_alignParentBottom="true"
android:layout_alignParentLeft="true"
android:text="LYLA"
android:textSize="24sp" />

<TextView
android:id="@+id/me_text_view"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_alignParentBottom="true"
android:layout_toRightOf="@id/lyla_text_view"
android:text="ME"
android:textSize="24sp" />

<TextView
android:id="@+id/natalie_text_view"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_alignParentLeft="true"
android:layout_above="@id/lyla_text_view"
android:text="NATALIE"
android:textSizee="24sp" />

<TextView
android:id="@+id/jennie_text_view"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_alignParentBottom="true"
android:layout_alignParentRight="true"
android:text="JENNIE"
android:textSize="24sp" />

<TextView
android:id="@+id/omoju_text_view"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_alignParentRight="true"
android:layout_above="@id/jennie_text_view"
android:text="OMOJU"
android:textSize="24sp" />

<TextView
android:id="@+id/amy_text_view"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_alignParentRight="true"
android:layout_above="@id/omoju_text_view"
android:text="AMY"
android:texxtSize="24sp" />

</RelativeLayout>
```

##RELATIVE LAYOUT WITH LIST ITEMS

```xml
<RelativeLayout
xmlns:android="http://schemas.android.com/apk/res/android"
android:layout_width="match_parent"
android:layout_height="match_parent">

<ImageView
android:id="@+id/photo_image_view"
android:layout_width="56dp"
android:layout_height="56dp"
android:src="@drawable/ocean"
android:scaleType="centerCrop" />

<TextView
android:id="@+id/pebble_text_view"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_toRightOf="@id/photo_image_view"
android:text="PEBBLE BEACH"
android:textAppearance="?android:textAppearanceMedium" />

<TextView
android:id="@+id/california_text_view"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_toRightOf="@id/photo_image_view
"
android:layout_below="@id/pebble_text_view"
android:text="CALIFORNIA"
android:textAppearance="?android:textAppearanceSmall" />

<TextView
android:id="@+id/miles_text_view"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_toRightof="@id/photo_image_view"
android:layout_below="@id/california_text_view"
android:text="10 MILES AWAY"
android:textAppearance="?android:textAppearanceSmall" />

</RelativeLayout   >
```

