# Webview

The Java port of the [webview/webview project](https://github.com/webview/webview). It uses JNA and auto-extracts the required dll/dylib/so libraries (v 0.12.0) for your current system.
Fork of the [webview/webview_java project](https://github.com/webview/webview_java)

<div align="center">
    <img alt="browser" src="demo.png" width="50%" />
    <br />
    <br />
</div>

## Examples

[Example](https://github.com/OldValencia/webview_java/blob/main/core/src/test/java/com/example/webview_java/Example.java)  
[Bridge Example](https://github.com/OldValencia/webview_java/blob/main/bridge/src/test/java/com/example/webview_java/BridgeExample.java)

## Supported Platforms

<table width=300>
    <tr>
        <td align="right" width=64>
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5f/Windows_logo_-_2012.svg/120px-Windows_logo_-_2012.svg.png?_=20220903072431" title="Windows" width="32" height="32">
        </td>
        <td align="left">
            x86, x86_64
        </td>
    </tr>
    <tr>
        <td align="right" width=64>
            <img src="https://simpleicons.org/icons/apple.svg" title="macOS" width="32" height="32">
        </td>
        <td align="left">
            aarch64, x86_64
        </td>
    </tr>
    <tr>
        <td align="right" width=64>
            <img src="https://simpleicons.org/icons/linux.svg" title="Linux" width="32" height="32">
        </td>
        <td align="left">
            x86, x86_64, arm, aarch64
        </td>
    </tr>
</table>

### Linux
Both MUSL and GLibC are supported out of the box. So it should work fine under distros like Debian, Arch, and Alpine.

### macOS
macOS requires that all UI code be executed from the first thread, which means you will need to launch Java with `-XstartOnFirstThread`. This also means that the Webview AWT helper will NOT work at all.
