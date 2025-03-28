cmake_minimum_required(VERSION 3.18)

project(SexyAppFramework)

include_directories(
    ${CMAKE_CURRENT_SOURCE_DIR}/../../lib/directx8
)

set(SRC_MAIN
	# Sources
	../ImageLib/ImageLib.cpp
	../ImageLib/jpeg/cdjpeg.c
	../ImageLib/jpeg/jcapimin.c
	../ImageLib/jpeg/jcapistd.c
	../ImageLib/jpeg/jccoefct.c
	../ImageLib/jpeg/jccolor.c
	../ImageLib/jpeg/jcdctmgr.c
	../ImageLib/jpeg/jchuff.c
	../ImageLib/jpeg/jcinit.c
	../ImageLib/jpeg/jcmainct.c
	../ImageLib/jpeg/jcmarker.c
	../ImageLib/jpeg/jcmaster.c
	../ImageLib/jpeg/jcomapi.c
	../ImageLib/jpeg/jcparam.c
	../ImageLib/jpeg/jcphuff.c
	../ImageLib/jpeg/jcprepct.c
	../ImageLib/jpeg/jcsample.c
	../ImageLib/jpeg/jctrans.c
	../ImageLib/jpeg/jdapimin.c
	../ImageLib/jpeg/jdapistd.c
	../ImageLib/jpeg/jdatadst.c
	../ImageLib/jpeg/jdatasrc.c
	../ImageLib/jpeg/jdcoefct.c
	../ImageLib/jpeg/jdcolor.c
	../ImageLib/jpeg/jddctmgr.c
	../ImageLib/jpeg/jdhuff.c
	../ImageLib/jpeg/jdinput.c
	../ImageLib/jpeg/jdmainct.c
	../ImageLib/jpeg/jdmarker.c
	../ImageLib/jpeg/jdmaster.c
	../ImageLib/jpeg/jdmerge.c
	../ImageLib/jpeg/jdphuff.c
	../ImageLib/jpeg/jdpostct.c
	../ImageLib/jpeg/jdsample.c
	../ImageLib/jpeg/jdtrans.c
	../ImageLib/jpeg/jerror.c
	../ImageLib/jpeg/jfdctflt.c
	../ImageLib/jpeg/jfdctfst.c
	../ImageLib/jpeg/jfdctint.c
	../ImageLib/jpeg/jidctflt.c
	../ImageLib/jpeg/jidctfst.c
	../ImageLib/jpeg/jidctint.c
	../ImageLib/jpeg/jidctred.c
	../ImageLib/jpeg/jmemmgr.c
	../ImageLib/jpeg/jmemnobs.c
	../ImageLib/jpeg/jquant1.c
	../ImageLib/jpeg/jquant2.c
	../ImageLib/jpeg/jutils.c
	../ImageLib/jpeg/rdbmp.c
	../ImageLib/jpeg/rdcolmap.c
	../ImageLib/jpeg/rdgif.c
	../ImageLib/jpeg/rdppm.c
	../ImageLib/jpeg/rdrle.c
	../ImageLib/jpeg/rdswitch.c
	../ImageLib/jpeg/rdtarga.c
	../ImageLib/jpeg/transupp.c
	../ImageLib/jpeg/wrbmp.c
	../ImageLib/jpeg/wrgif.c
	../ImageLib/jpeg/wrppm.c
	../ImageLib/jpeg/wrrle.c
	../ImageLib/jpeg/wrtarga.c
	../ImageLib/png/png.c
	../ImageLib/png/pngerror.c
	../ImageLib/png/pngget.c
	../ImageLib/png/pngmem.c
	../ImageLib/png/pngpread.c
	../ImageLib/png/pngread.c
	../ImageLib/png/pngrio.c
	../ImageLib/png/pngrtran.c
	../ImageLib/png/pngrutil.c
	../ImageLib/png/pngset.c
	../ImageLib/png/pngtrans.c
	../ImageLib/png/pngvcrd.c
	../ImageLib/png/pngwio.c
	../ImageLib/png/pngwrite.c
	../ImageLib/png/pngwtran.c
	../ImageLib/png/pngwutil.c
	../ImageLib/zlib/adler32.c
	../ImageLib/zlib/compress.c
	../ImageLib/zlib/crc32.c
	../ImageLib/zlib/deflate.c
	../ImageLib/zlib/gzio.c
	../ImageLib/zlib/infblock.c
	../ImageLib/zlib/infcodes.c
	../ImageLib/zlib/inffast.c
	../ImageLib/zlib/inflate.c
	../ImageLib/zlib/inftrees.c
	../ImageLib/zlib/infutil.c
	../ImageLib/zlib/trees.c
	../ImageLib/zlib/uncompr.c
	../ImageLib/zlib/zutil.c
	../PakLib/PakInterface.cpp
	
	Color.cpp
	Font.cpp
	Graphics.cpp
	NativeDisplay.cpp
	Image.cpp
	ImageFont.cpp
	MemoryImage.cpp
	SysFont.cpp
	TTFFont.cpp
	Quantize.cpp
	SharedImage.cpp

	Flags.cpp
	XMLParser.cpp
	SexyMatrix.cpp
	SEHCatcher.cpp
	PropertiesParser.cpp
	PerfTimer.cpp
	MTRand.cpp
	KeyCodes.cpp
	HTTPTransfer.cpp
	DirectXErrorString.cpp
	Debug.cpp
	CritSect.cpp
	Common.cpp
	Buffer.cpp
	ResourceManager.cpp
	ModVal.cpp
	DescParser.cpp
	Ratio.cpp

	ogg/bitwise.c
	ogg/block.c
	ogg/codebook.c
	ogg/floor0.c
	ogg/floor1.c
	ogg/framing.c
	ogg/info.c
	ogg/mapping0.c
	ogg/mdct.c
	ogg/registry.c
	ogg/res012.c
	ogg/sharedbook.c
	ogg/synthesis.c
	ogg/vorbisfile.c
	ogg/window.c
	SexyAppBase.cpp

	DSoundManager.cpp
	DSoundInstance.cpp
	BassLoader.cpp
	BassMusicInterface.cpp
	FModLoader.cpp
	FModMusicInterface.cpp
	FModSoundInstance.cpp
	MusicInterface.cpp
	
	SWTri.cpp
	WidgetManager.cpp
	Widget.cpp
	TextWidget.cpp
	Slider.cpp
	ScrollbuttonWidget.cpp
	ScrollbarWidget.cpp
	ListWidget.cpp
	Insets.cpp
	HyperlinkWidget.cpp
	EditWidget.cpp
	Checkbox.cpp
	ButtonWidget.cpp
	Dialog.cpp
	DialogButton.cpp
	FlashWidget.cpp
	WidgetContainer.cpp

	# Headers
	../ImageLib/ImageLib.h
	../ImageLib/jpeg/cderror.h
	../ImageLib/jpeg/cdjpeg.h
	../ImageLib/jpeg/jchuff.h
	../ImageLib/jpeg/jconfig.h
	../ImageLib/jpeg/jdct.h
	../ImageLib/jpeg/jdhuff.h
	../ImageLib/jpeg/jerror.h
	../ImageLib/jpeg/jinclude.h
	../ImageLib/jpeg/jmemsys.h
	../ImageLib/jpeg/jmorecfg.h
	../ImageLib/jpeg/jpegint.h
	../ImageLib/jpeg/jpeglib.h
	../ImageLib/jpeg/jversion.h
	../ImageLib/jpeg/transupp.h
	../ImageLib/png/png.h
	../ImageLib/png/pngasmrd.h
	../ImageLib/png/pngconf.h
	../ImageLib/zlib/deflate.h
	../ImageLib/zlib/infblock.h
	../ImageLib/zlib/infcodes.h
	../ImageLib/zlib/inffast.h
	../ImageLib/zlib/inffixed.h
	../ImageLib/zlib/inftrees.h
	../ImageLib/zlib/infutil.h
	../ImageLib/zlib/trees.h
	../ImageLib/zlib/zconf.h
	../ImageLib/zlib/zlib.h
	../ImageLib/zlib/zutil.h
	../PakLib/PakInterface.h
	AutoCrit.h
	BassLoader.h
	BassMusicInterface.h
	Buffer.h
	ButtonListener.h
	ButtonWidget.h
	Checkbox.h
	CheckboxListener.h
	Color.h
	Common.h
	CritSect.h
	Debug.h
	Dialog.h
	DialogButton.h
	DialogListener.h
	DirectXErrorString.h
	DSoundInstance.h
	DSoundManager.h
	EditListener.h
	EditWidget.h
	Flags.h
	FlashWidget.h
	FModLoader.h
	FModMusicInterface.h
	FModSoundInstance.h
	FModSoundManager.h
	Font.h
	Graphics.h
	HTTPTransfer.h
	HyperlinkWidget.h
	Image.h
	ImageFont.h
	Insets.h
	KeyCodes.h
	ListListener.h
	ListWidget.h
	memmgr.h
	MemoryImage.h
	ModVal.h
	MTRand.h
	MusicInterface.h
	NativeDisplay.h
	ogg/asm_arm.h
	ogg/backends.h
	ogg/codebook.h
	ogg/codec_internal.h
	ogg/config_types.h
	ogg/ivorbiscodec.h
	ogg/ivorbisfile.h
	ogg/lsp_lookup.h
	ogg/mdct.h
	ogg/mdct_lookup.h
	ogg/misc.h
	ogg/ogg.h
	ogg/os.h
	ogg/os_types.h
	ogg/registry.h
	ogg/window.h
	ogg/window_lookup.h
	PerfTimer.h
	Point.h
	PropertiesParser.h
	Quantize.h
	Rect.h
	ResourceManager.h
	ScrollbarWidget.h
	ScrollbuttonWidget.h
	ScrollListener.h
	SEHCatcher.h
	SexyAppBase.h
	SexyMatrix.h
	SexyVector.h
	Slider.h
	SliderListener.h
	SmartPtr.h
	SoundInstance.h
	SoundManager.h
	SWTri.h
	SysFont.h
	TTFFont.h
	TextWidget.h
	Widget.h
	WidgetContainer.h
	WidgetManager.h
	XMLParser.h

	SDLImage.cpp
	SDLInterface.cpp

	SDLImage.h
	SDLInterface.h
)

add_compile_definitions(SexyAppFramework _LIB)
add_library(SexyAppFramework STATIC ${SRC_MAIN})

include(FetchContent)

FetchContent_Declare(
        SDL3
        GIT_REPOSITORY https://github.com/libsdl-org/SDL
        # This will be a tag once SDL3 is released
        GIT_TAG origin/main
    )
FetchContent_MakeAvailable(SDL3)

FetchContent_Declare(
        SDL3_ttf
        GIT_REPOSITORY https://github.com/libsdl-org/SDL_ttf
        GIT_TAG origin/main
    )
FetchContent_MakeAvailable(SDL3_ttf)

set(SexyAppLibs
	SDL3::SDL3
	SDL3_ttf::SDL3_ttf
	${CMAKE_CURRENT_SOURCE_DIR}/../../lib/directx8/d3d8.lib
	dsound
	winmm
	ws2_32
)
target_link_libraries(SexyAppFramework ${SexyAppLibs})
