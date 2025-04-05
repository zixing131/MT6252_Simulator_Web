

main:
	emcc -Os -Wall ../src/main.c ../src/mysocket.c ../src/myui.c ../src/socket.c \
		./unicorn/libunicorn.a \
		-s EXPORTED_FUNCTIONS="['_main', '_malloc', '_free']" \
		-s TOTAL_MEMORY=512MB \
		-s USE_SDL=2 \
		-Wno-unsequenced \
		-Wno-int-conversion \
		-Wno-enum-conversion \
		-Wno-unused-variable \
		-Wno-return-type \
		-Wno-incompatible-pointer-types \
		-Wno-incompatible-function-pointer-types \
		-Wno-implicit-function-declaration \
		-Wno-format \
		-Wno-pointer-sign \
		-Wno-macro-redefined \
		-Wno-compare-distinct-pointer-types \
		-Wno-shift-overflow \
		-Wno-parentheses \
		-s USE_ZLIB=1 \
		-s WASM=1 \
		-s FORCE_FILESYSTEM=1 \
		-pthread \
		-s PROXY_TO_PTHREAD=1 \
		-s USE_PTHREADS=1 \
		-s PTHREAD_POOL_SIZE=7 \
		-sSHARED_MEMORY=1 \
		-matomics \
		-mbulk-memory \
		-s VERBOSE=1 \
		-o dist2/mtsim.html \
		--preload-file Rom\08000000.bin 
		