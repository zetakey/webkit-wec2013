# webkit-winec2013
Webkit port for Windows Embedded Compact 2013  
This project takes the inactive Windows CE Port of WebKit[https://trac.webkit.org/wiki/WinCE#no1] and repackage it to Microsoft's Windows Embedded Compact 2013  

Build Procedure
---------------
1.  Merge all changes in source 

2.  Build WINCE5 as in webkit wince port
[https://trac.webkit.org/wiki/WinCE#no1]

3.  Global changes in webkitbuild:

  WTF_CPU_ARM_TRADITIONAL => WTF_CPU_ARM_THUMB2 for all vc project files  
  _WIN32_WCE=0x500; => _WIN32_WCE=0x800;  
  Visual Studio 8 2005 =>  Microsoft Visual Studio 11.0   
  STANDARDSDK_500 (ARMV4I) => to whatever available in your wince 2013 sdk  
  C:\Program Files\Microsoft Visual Studio 8\VC\ce\bin\x86_arm\cl.exe  => c:\Program Files\Microsoft Visual Studio 11.0\VC\BIN\x86_ARM\cl.exe  
  --prefix=MSVC  = > --prefix=MSVCTHUMB   


4.  Open webkit.sln and then build Release ALL_BUILD

Contact info
------------
Email: contact@zetakey.com  
Website: http://www.zetakey.com  
