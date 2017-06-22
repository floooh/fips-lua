if (NOT FIPS_IMPORT)
    cmake_minimum_required(VERSION 2.8)
    get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
    include("${FIPS_ROOT_DIR}/cmake/fips.cmake")
    fips_setup(PROJECT lua)
endif()

fips_begin_lib(lua)
    fips_dir(lua)
    fips_files(
        lua.h
        lapi.c
        lapi.h
        lauxlib.c
        lauxlib.h
        lbaselib.c
        lbitlib.c
        lcode.c
        lcode.h
        lcorolib.c
        lctype.c
        lctype.h
        ldblib.c
        ldebug.c
        ldebug.h
        ldo.c
        ldo.h
        ldump.c
        lfunc.c
        lfunc.h
        lgc.c
        lgc.h
        linit.c
        liolib.c
        llex.c
        llex.h
        llimits.h
        lmathlib.c
        lmem.c
        lmem.h
        loadlib.c
        lobject.c
        lobject.h
        lopcodes.c
        lopcodes.h
        loslib.c
        lparser.c
        lparser.h
        lprefix.h
        lstate.c
        lstate.h
        lstring.c
        lstring.h
        lstrlib.c
        ltable.c
        ltable.h
        ltablib.c
        ltests.c
        ltests.h
        ltm.c
        ltm.h
        luaconf.h
        lualib.h
        lundump.c
        lundump.h
        lutf8lib.c
        lvm.c
        lvm.h
        lzio.c
        lzio.h
    )
fips_end_lib()

if (NOT FIPS_IMPORT)
    fips_finish()
endif()


