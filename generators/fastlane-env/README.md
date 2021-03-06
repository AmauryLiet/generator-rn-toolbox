# Fastlane Environment Generator

## Usage

### 1. Create a new Environment
```
yo rn-toolbox:fastlane-env
```

### 2. Generate the provisioning profiles
```
bundle exec fastlane ios setup --env=<myenv>
```

### 3. AppStore Setup (Appstore Deployment only)
- AppStore deployment will require app icons to be setup
- Right now iTunes Connect automatic app creation has been disabled due to issues and will necessitate manual setup
  - Head to [iTunes Connect](https://itunesconnect.apple.com/)
  - Create a new app using the app id you provided

### 4. Deploy your app
***:warning: Automatic Play Store deployment is not yet available (PR welcome!)***
```
bundle exec fastlane ios deploy --env=<myenv>
bundle exec fastlane android deploy --env=<myenv>
```

## Centralizing environment variables
You might want to share some environment variables accross multiple environments. In order to do so, simply create a `.env` file, remove the variable you want to share in all the environment files and add it in the `.env` one.
