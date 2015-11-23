# Swift — Creating A File

## Objectives

1. Create a Swift file in Xcode with the correct target membership.
2. Understand the basic nature of modules and importing in Swift.

## Introduction

True to the pattern of object-oriented programming, programming in Swift follows the pattern of breaking code into smaller files to make them easier to navigate and maintain. A Swift file can house a variety of elements, each of which are justifiable to put into a dedicated file.

Most commonly, a file is synonymous with a custom class. However, a class's file may also appropriately hold an enum, a struct, or a global function that is closely associated with that class. Extensions, global functions, enums, and structs may also be appropriately placed in their own files.

**Objective-C:** *Developers familiar with Objective-C will note that Swift's files are somewhat more freeform in their nature than files in Objective-C. The header/implementation file dualism is also gone, since Swift handles visibility in a different pattern known as modules. Modules also make class prefixing unnecessary, so learning a Swift "accent" includes dropping class prefixes.*

## Creating A File

In general, creating a custom class should be synonymous with creating a file to hold it. The steps to create an empty file are unsurprisingly straightforward:

1. Select your project's group in the Project Navigator. You *can* move a file around between groups after creating it, but having the desired group selected will load the appropriate targets in the setup menus:

    ![](https://curriculum-content.s3.amazonaws.com/swift/swift-creating-a-file/create_file_select_group.png)
    
2. Select `File` --> `New` --> `File...` from the taskbar when Xcode is the active application:
    
    ![](https://curriculum-content.s3.amazonaws.com/swift/swift-creating-a-file/create_file_menu_new_file.png)


3. Select `iOS` --> `Source` --> `Swift File`, then click `Next`:

    ![](https://curriculum-content.s3.amazonaws.com/swift/swift-creating-a-file/create_file_choose_source_swift.png)

4. Enter the name of the file to create, which should be named for its intended contents. The current project's folder should be selected as the destination (this will determine which *directory* the file is created in), the desired group can be selected as well (this is where your new file which appear in your Project Navigator), and the file's Target membership can be selected (which as a default should be only your project unless you are creating a test file). Click `Create` when you are ready:

    ![](https://curriculum-content.s3.amazonaws.com/swift/swift-creating-a-file/create_file_name_file.png)

5. Xcode should now generate the file and automatically navigate you to its empty contents in the Code Editor:

    ![](https://curriculum-content.s3.amazonaws.com/swift/swift-creating-a-file/create_file_created_file.png)
    
From here you can add the desired contents to the file. 
    
## Module Basics
    
Dependencies on other files within the same project do not need to be imported like in Objective-C, though importing outside frameworks such as `UIKit` or any Cocoapods do need to be explicitly imported. Non-private properties and methods in the same module are visible "internally" and are available to other files in the same module by default.

You'll notice that `AppDelegate.swift` file imports `UIKit` (`UIKit` contains `Foundation` which is implicitly imported as part of `UIKit`), making use of `UIResponder`, `UIApplicationDelegate`, `UIWindow`, and `UIApplication`. You shouldn't need to add import statements until you begin working outside the `Foundation` framework.

![](https://curriculum-content.s3.amazonaws.com/swift/swift-creating-a-file/AppDelegate_imports_UIKit.png)


