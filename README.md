# cocos2d_libs_generate

Helps to migrate cocos2d-x v3.x => v4.x.
or helps to build project using cocos2d-x v4.x on Xcode.

## Migrate with prebuild (for cocos2d-x 4.0)

1. generate new project with cocos2d-x 4.0
1. copy `cocos2d` directory in the new project into your old project and replace.
1. copy `build/cocos2d_libs.xcconfig` and `prebuild/cocos2d_libs.xcodeproj` (from this repo) into your project like below.

```
cocos2d
├── build
│   ├── cocos2d_libs.xcconfig
│   └── cocos2d_libs.xcodeproj
```

4. fix compile errors.

## Generate cocos2d_libs.xcodeproj by myself

### Requirements

- [XcodeGen](https://github.com/yonaskolb/XcodeGen) 2.11.0 or above

### Generate

```
git clone https://github.com/sidepelican/cocos2d_libs_generate.git
cd cocos2d_libs_generate
cp -r build <your cocos2d-x project>/cocos2d
cd <your cocos2d-x project>/cocos2d/build
xcodegen generate
```