# Drag LinearLayout

An Android LinearLayout that supports draggable and swappable child Views.

## Add it to your project using Gradle:

```dependency
implementation 'com.jmedeisis:draglinearlayout:1.1.0'
```

## main_activity.xml

```xml
<?xml version="1.0" encoding="utf-8"?>
<com.jmedeisis.draglinearlayout.DragLinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:id="@+id/container"
    android:layout_alignParentTop="true"
    tools:context=".MainActivity">
    <TextView
        android:id="@+id/text"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="10dp"
        android:text="@string/hello_raushan"
        android:textColor="@color/white"
        android:textSize="30sp"
        android:background="#6EDA00"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        android:gravity="center_horizontal" />

    <ImageView
        android:layout_width="match_parent"
        android:layout_height="200dp"
        android:src="@drawable/my_logo"
        android:background="#6EDA00"
        android:layout_marginTop="20dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        android:contentDescription="@string/desc" />

    <TextView
        android:id="@+id/text2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="10dp"
        android:text="@string/bye_raushan"
        android:textColor="@color/white"
        android:textSize="30sp"
        android:background="#6EDA00"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        android:gravity="center_horizontal" />


</com.jmedeisis.draglinearlayout.DragLinearLayout>
```

## Java class important code
```java

        DragLinearLayout dragLinearLayout=findViewById(R.id.container);
        for(int i=0;i<dragLinearLayout.getChildCount();i++)
        {
            View child=dragLinearLayout.getChildAt(i);

            dragLinearLayout.setViewDraggable(child,child);
        }
```
## Limitation
Supports only the LinearLayout#VERTICAL orientation.

