# KDMapper

Original creator https://github.com/z175

Updated and improved by https://github.com/TheCruZ

Tested from **Windows 10 1607** to current **Windows 10 21H1** (and up to v21354) :heavy_check_mark:

Update mainly done for UnknownCheats Forum https://www.unknowncheats.me/forum/members/1117395.html

KDMapper is a simple tool that exploits iqvw64e.sys Intel driver to manually map non-signed drivers in memory

Fixups:

    Hook "NtQueryInformationAtom" which exists in all windows versions
    Fixed unable to load /GS- compiled drivers

Improvements:

	Implemented NtLoadDriver and NtUnloadDriver for less traces
	Prevent load if \Device\Nal exists (Prevents BSOD)
	Automatic clear PiDDBCacheTable
	Header section skipped while copying driver to kernel
	Automatic clear g_KernelHashBucketList
	
Requirements:

    Set Custom Driver Entry Point
    Create a thread and return from driver entry fastest as you can to prevent unexpected calls

Have Fun!!
