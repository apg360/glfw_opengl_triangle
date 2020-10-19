# glfw_opengl_triangle
## triangle-opengl.c from GLFW examples folder

## How to build

* ### Platform
  * #### macOS Catalina 10.15.6 :
	<details>
	<summary>Build commands</summary>
	
	  ##### Links :
          
	  - If `xcode-select` does not work, download dmg file manually : [Command_Line_Tools_for_Xcode_12.dmg](https://download.developer.apple.com/Developer_Tools/Command_Line_Tools_for_Xcode_12/Command_Line_Tools_for_Xcode_12.dmg)
	  - Also work with GM version. GM suffix means Gold Master, the final build before distribution of the official release.
                         [Command_Line_Tools_for_Xcode_12_GM_seed.dmg](https://download.developer.apple.com/Developer_Tools/Command_Line_Tools_for_Xcode_12_GM_seed/Command_Line_Tools_for_Xcode_12_GM_seed.dmg)
	  - Apple Developer website : [Command_Line_Tools_for_Xcode](https://developer.apple.com/download/more/?=command%20line%20tools)
	  - [clang+llvm-10.0.0-x86_64-apple-darwin.tar.xz](https://github.com/llvm/llvm-project/releases/download/llvmorg-10.0.0/clang+llvm-10.0.0-x86_64-apple-darwin.tar.xz)
   
   
	  ##### Steps :
                   
        xcode-select reset && xcode-select --install
    
        brew install ninja cmake
    
        Download Pre-Built Binaries and untar in your project directory clang+llvm-10.0.0-x86_64-apple-darwin.tar.xz
        
        in zsh terminal, make sure to be in the project directory, do :  ./compile.sh
    
	</details>
