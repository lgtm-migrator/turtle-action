# 🐢 turtle-action

[![GitHub Workflow Status](https://img.shields.io/github/workflow/status/nzws/turtle-action/Node%20CI?style=for-the-badge)](https://github.com/nzws/turtle-action/actions)
[![GitHub](https://img.shields.io/github/license/nzws/turtle-action?style=for-the-badge)](#license)
[![code style: Prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=for-the-badge&logo=prettier)](https://prettier.io/)
[![dependabot enabled](https://img.shields.io/badge/dependabot-enabled-0366D6.svg?style=for-the-badge&logo=dependabot)](https://github.com/nzws/turtle-action/pulls?utf8=%E2%9C%93&q=is%3Apr+label%3Adependencies+)

> 🐢 Turtle CLI with GitHub Actions for building expo-project

- [ ] Android
- [ ] iOS

# Usage

In workflow:

## Android

```yaml
- uses: nzws/turtle-action@v1
  with:
    build_os: 'android'
    expo_sdk_version: '36.0.0' # your SDK version
  env:
    EXPO_ANDROID_KEYSTORE_BASE64: ${{ secrets.EXPO_ANDROID_KEYSTORE_BASE64 }}
    EXPO_ANDROID_KEYSTORE_ALIAS: ${{ secrets.EXPO_ANDROID_KEYSTORE_ALIAS }}
    EXPO_ANDROID_KEYSTORE_PASSWORD: ${{ secrets.EXPO_ANDROID_KEYSTORE_PASSWORD }}
    EXPO_ANDROID_KEY_PASSWORD: ${{ secrets.EXPO_ANDROID_KEY_PASSWORD }}
```

## iOS

```yaml
- uses: nzws/turtle-action@v1
  with:
    build_os: 'ios'
    expo_sdk_version: '36.0.0' # your SDK version
  env:
    EXPO_APPLE_TEAM_ID: ${{ secrets.EXPO_APPLE_TEAM_ID }}
    EXPO_IOS_DIST_P12_BASE64: ${{ secrets.EXPO_IOS_DIST_P12_BASE64 }}
    EXPO_IOS_DIST_P12_PASSWORD: ${{ secrets.EXPO_IOS_DIST_P12_PASSWORD }}
    EXPO_IOS_PROVISIONING_PROFILE_BASE64: ${{ secrets.EXPO_IOS_PROVISIONING_PROFILE_BASE64 }}
```

# License

- code: MIT
