
# 🦄 SwiftFormat and SwiftLint Setup Guide 

This guide will help you set up SwiftFormat and SwiftLint in your Swift project for automated code formatting and linting.



## Run Locally



```bash
  chmod +x format_and_lint.sh
```

Install dependencies

```bash
  ./format_and_lint.sh
```
 
 


## 1. Clone or Download Files

 Clone or download the necessary files from the https://github.com/gonz4216/Fortmat-and-lint-for-Swift.


## 2. Copy Configuration Files

Copy the following files from the downloaded repository to your Swift project's directory:




- **`.swift-version`**
- **`.swiftformat`**
- **`format_and_lint.sh`**
- **`README.md`**
 
 ## 3. Add Build Phase in Xcode
  1. Open your Xcode project.
    
  2. In the Xcode project navigator, select your project.
    
  3. Go to the project's target (the one you want to lint) and select "Build Phases."
    
  4. Click the "+" button and choose "New Run Script Phase."
    
  5. In the newly created "Run Script" phase, add the following script:



 
```shell
if [[ "$(uname -m)" == arm64 ]]; then
    export PATH="/opt/homebrew/bin:$PATH"
fi

if which swiftlint > /dev/null; then
    swiftlint
else
    echo "warning: SwiftLint not installed, download from https://github.com/realm/SwiftLint"
fi


```



## 4. Give Permissions in Terminal
    
1. Open Terminal.
    
2. Navigate to your project directory using the **`cd`** command.
    
3. Provide execute permissions to the  format_and_lint.sh script:
    

 
```shell
chmod +x format_and_lint.sh
```
 

 ## 5. Run the Script 
 
 1. In Terminal, within your project directory, run the script:
```shell
./format_and_lint.sh
```

## Enjoy Programming!

You've successfully set up SwiftFormat and SwiftLint in your Swift project. Now, enjoy coding with automated code formatting and linting!
