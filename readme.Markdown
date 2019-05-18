# 实验四
## **实验内容：**   
#### 使用PrefereceFragment实现设置页面
#### 设置项说明  
总共四组设置项　

In-line preferences  
　　CheckBoxPreference  
Dialog-based preferences:  
　　EditTextPreference  
　　ListPreference
Launch preferences  
　　PreferenceScreen: 跳转到另一个PreferenceScreen  
　　PreferenceScreen: 启动一个网页
Preference attributes  
　　CheckBox: 父选项  
　　CheckBox: 子选项，当父选项勾选时呈现
## **主要代码：**  
#### preference.xml
```javascript
<PreferenceScreen
xmlns:android="http://schemas.android.com/apk/res/android">
    <PreferenceCategory
        android:title="ln-line preferences"
        android:key="category_1">
        <CheckBoxPreference
            android:key="checkBox_1"
            android:summary="This is a checkbox"
            android:title="Checkbox preference"
            android:defaultValue="false" />
    </PreferenceCategory>

    <PreferenceCategory
        android:key="category_2"
        android:title="Dialog-based preferences">
        <EditTextPreference
            android:key="edittext_1"
            android:title="Edit text preference"
            android:summary="An example that uses an edit text dialog"/>
        <ListPreference
            android:key="list_1"
            android:title="List preference"
            android:summary="An example that uses a list dialog"
            android:dialogTitle="Choose One"
            android:entries="@array/number"
            android:entryValues="@array/number1"/>
    </PreferenceCategory>

    <PreferenceCategory
        android:key="category_3"
        android:title="Launch preferences">
        <PreferenceScreen
            android:key="scream_1"
            android:title="Scream preference"
            android:summary="Shows another screen of preferences">
            <PreferenceScreen
                android:title="Toggle preference"
                android:summary="preference that is on the next scream but same hierarchy"/>
        </PreferenceScreen>

        <PreferenceScreen
            android:key="scream_2"
            android:title="Intent preference"
            android:summary="Launches an Activity from an Intent">
            <intent android:action="android.intent.action.VIEW"
                android:data="http://www.baidu.com"/>
        </PreferenceScreen>
    </PreferenceCategory>

    <PreferenceCategory
        android:key="category_3"
        android:title="Preference attributes">
        <CheckBoxPreference
            android:key="checkBox_2"
            android:title="Parent checkbox preference"
            android:summary="This is visually parent" />
        <CheckBoxPreference
            android:key="checkBox_3"
            android:title="Child checkbox preference"
            android:summary="This is visually child"
            android:dependency="checkBox_2"/>
    </PreferenceCategory>
</PreferenceScreen>

``` 
## **实验截图：**
### 基本界面
![Alt](https://github.com/CunmingChen/Android/blob/master/AndroidTest/ExtendedActivity/pic1.png?raw=true#pic_center)
![Alt](https://github.com/CunmingChen/Android/blob/master/AndroidTest/ExtendedActivity/pic2.png?raw=true#pic_center)
### 界面截图1
![Alt](https://github.com/CunmingChen/Android/blob/master/AndroidTest/ExtendedActivity/pic3.png?raw=true#pic_center)
### 界面截图2 
![Alt](https://github.com/CunmingChen/Android/blob/master/AndroidTest/ExtendedActivity/pic4.png?raw=true#pic_center)
### 界面截图3 
![Alt](https://github.com/CunmingChen/Android/blob/master/AndroidTest/ExtendedActivity/pic5.png?raw=true#pic_center)  
### 界面截图4  
![Alt](https://github.com/CunmingChen/Android/blob/master/AndroidTest/ExtendedActivity/pic6.png?raw=true#pic_center)  
### 界面截图5 
![Alt](https://github.com/CunmingChen/Android/blob/master/AndroidTest/ExtendedActivity/pic7.png?raw=true#pic_center)  
