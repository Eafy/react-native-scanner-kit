# react-native-scanner-kit[![npm version](https://img.shields.io/npm/v/react-native-scanner-kit.svg?style=flat)](https://www.npmjs.com/package/react-native-scanner-kit)

QR Scanner Kit for React Native(Android & iOS), support react native 0.57.8+

### Environments 环境要求
1.JS
- node: 8.0+

2.iOS
- XCode: 9.0+

3.Android
- Android SDK: api 28+
- gradle: 4.5
- Android Studio: 3.1.3+

### npm源
`npm install react-native-scanner-kit --save`

### 原生模块导入
#### Android Studio
`react-native link react-native-scanner-kit`

#### iOS/Xcode
使用 pod

Podfile 增加
```
  pod 'React', :path => '../node_modules/react-native', :subspecs => [
    'Core',
    'CxxBridge',
    'DevSupport', 
    'RCTText',
    'RCTNetwork',
    'RCTWebSocket', 
    'RCTAnimation'
  ]
  pod 'yoga', :path => '../node_modules/react-native/ReactCommon/yoga'
  pod 'DoubleConversion', :podspec => '../node_modules/react-native/third-party-podspecs/DoubleConversion.podspec'
  pod 'glog', :podspec => '../node_modules/react-native/third-party-podspecs/glog.podspec'
  pod 'Folly', :podspec => '../node_modules/react-native/third-party-podspecs/Folly.podspec'

  pod 'react-native-scanner-kit', :podspec => '../node_modules/react-native-scanner-kit/ios/react-native-scanner-kit.podspec'
```
### Usage 使用方法
`import { QRSannerView } from 'react-native-scanner-kit';`

#### QRScannerView Props 属性
| Prop                    | Type  | Default  | Description
| ----------------------- |:-----:| :-------:| -------
| cropRect                | object| full     | Scanning area
| isStartScan             | bool  | true     |
| isOpenFlash             | bool  | false    |
| scanAudioFile           | string| null     | 
| rereadQR                | object| {reread: true,time: 1.0} | 
| onScanResult            | func  | undefined| 
| onScanError             | func  | undefined|
