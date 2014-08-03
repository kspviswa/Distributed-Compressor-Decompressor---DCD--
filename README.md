Distributed-Compressor-Decompressor---DCD--
===========================================

Distributed Compressor / Decompress-or [DCD] will perform file compression / decompression in distributed fashion.

The file compression / decompression will be accomplished by ZLIB library.
Interesting fact about this tool is that, it manages to accomplish the task
under distributed fashion, thereby taking more load in parallel.

Typical applications would be using this tool to quickly compress the files, before uploading to storage servers etc.

Following binaried planned for this project.

1) Client tool ---> Which takes the file name as input and trigger the task to server.
2) Server tool ---> Which runs in multithreaded mode to parallely compress files in distributed fashion.
3) Server peers tool --> Which runs in sync with other server peers [either in same machine / different machines], communicates via IPC / RPC / Sockets to share the load.
4) Monitoring tool / webpage to present the status of the server peers.
