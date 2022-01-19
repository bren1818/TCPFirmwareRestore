# TCPFirmwareRestore (Deprecated)
Connected By TCP - Greenwave Reality Bridge Firmware - for restoring/re-flashing

This project is based on https://github.com/hypergolic/greeenwave_firmware however I will include a step by step instruction on how to downgrade the firmware for people who have limited understanding of networking or programming or just need a bit of extra help.

I am adding the project as recently my bridge simply stopped working. I hadn't modified the firmware, or even done anything with it which should have caused the issue, however, suddenly it would no longer allow me to use the 'sync' button, as such I could not generate tokens or use the bridge with my other project here: https://github.com/bren1818/TCPLightingWebInterface

I tried to use hypergolic's files (which did eventually work for me) however I had a great deal of trouble getting my low end consumer grade router to work since it couldn't re-write requests. To get it to go, I downloaded a trial of Simple DNS Plus http://simpledns.com/ and created records for update.greenwavereality.com and update.greenwavereality.eu and pointed them to my local machine where I was running the python server. I then pointed my router's DNS settings to my local machine. My local machine had simple dns running on it, and had it's host files write the following entries to the local machine (127.0.0.1):

127.0.0.1 greenwavereality.eu
127.0.0.1 greenwavereality.com
127.0.0.1 update.greenwavereality.com
127.0.0.1 update.greenwavereality.eu

I then was able to use hypergolic's project but had to restore a lower version of the firmware 2.0.47 versus the 3.0.39 firmware hypergolic provided to make my bridge work again. Now everything is swell. I'm going to author a more thorough tutorial of how to accomplish the task and include it here. For now, here are the firmware files etc...

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <http://unlicense.org>

