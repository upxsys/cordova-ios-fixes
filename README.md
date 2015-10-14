# cordova-ios-application-queries-schemes
`cordova plugin add cordova-ios-application-queries-schemes`
or
`cordova plugin add https://github.com/chancezeus/cordova-ios-application-queries-schemes.git`

There are issues with the Cordova InAppBrowser plugin when opening facebook url's in the system browser
(http[s]://[www.]facebook.com), these errors seem to be related to iOS first resolving the deep link and then
checking against the whitelist (and thus throwing an error on canOpenUrl), even when you try to open the
website instead of the app.

It will add the following part to the `*-Info.plist` file during build process:

    <key>LSApplicationQueriesSchemes</key>
    <array>
        <string>fb</string>
        <string>gplus</string>
        <string>instagram</string>
        <string>kindle</string>
        <string>linkedin</string>
        <string>pinterest</string>
        <string>tumblr</string>
        <string>twitter</string>
        <string>whatsapp</string>
        <string>yelp</string>
        <string>youtube</string>
    </array>
