# Customise-exoplayer

Dependencies: 
    implementation 'com.google.android.exoplayer:exoplayer-core:2.8.2'
    implementation 'com.google.android.exoplayer:exoplayer-dash:2.8.2'
    implementation 'com.google.android.exoplayer:exoplayer-ui:2.8.2'


We need to add Manifest in,
        android:largeHeap="true"
        android:requestLegacyExternalStorage="true"
        android:networkSecurityConfig="@xml/network_config"
        android:usesCleartextTraffic="true"
        
And add create xml file and add its line,
<?xml version="1.0" encoding="utf-8"?>
<network-security-config>
    <base-config cleartextTrafficPermitted="true">
        <trust-anchors>
            <certificates src="system" />
        </trust-anchors>
    </base-config>
</network-security-config>.

No add its line then player not load url.
