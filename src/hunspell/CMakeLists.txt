set(SRC
    affixmgr.cxx
    csutil.cxx
    hashmgr.cxx
    hunspell.h
    hunzip.cxx
    phonet.hxx
    suggestmgr.hxx
    affixmgr.hxx
    csutil.hxx
    hashmgr.hxx
    hunspell.hxx
    hunzip.hxx
    replist.cxx
    utf_info.hxx
    affentry.cxx
    atypes.hxx
    filemgr.cxx
    htypes.hxx
    hunvisapi.h
    langnum.hxx
    replist.hxx
    w_char.hxx
    affentry.hxx
    baseaffix.hxx
    filemgr.hxx
    hunspell.cxx
    phonet.cxx
    suggestmgr.cxx)

add_compile_options("-DBUILDING_LIBHUNSPELL")
add_library(hunspell SHARED ${SRC})
target_include_directories(hunspell PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
set_target_properties(hunspell PROPERTIES PUBLIC_HEADER "hunspell.hxx;hunspell.h")
install(TARGETS hunspell)
