# drawingpp_Chelsi
Chelsi's code examples on drawing with the body for Fall 2022 MIT Media Lab drawing++ class 

## How to re-build in Xcode
Avoid re-building with projectGenerator unless absolutely necessary

If you need to rebuild using projectGenerator follow the following steps:

1. Go to File > Project Settings > Build System -> New Build System
2. In the left sidebar, click on the Project Name > Go to General tab > Find Frameworks, Libraries, and Embedded Content -> Add the following frameworks using the '+':
- Vision
- CoreML
- AVKit
- AVFoundation
- Foundation
3. Still in Project Name > General > Find Deployemnt Info -> Change Deployment Target to 11.3
4. Still in Project Name >  Go to Build Phases tab > Find Link Binary with Libraries -> Change "mac catalyst" to "always"

For each file in src folder, on right sidebar, change file "Type" to Objective C++ (not extension, just in the dropdown menu in right sidebar)

If you encounter Undefined symbol: __objc_msgSend$identifier, you might need to set Excluded Architectures arm64. See this issue for details.

If there're some complaints about ARC, you might need to remove all mentions of autorelease in src folder.
