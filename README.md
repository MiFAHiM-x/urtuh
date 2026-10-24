
### 1. Privilege escalation
- **Method 1:** [https://rootme.wssllhdg.dpdns.org/lonStack/CVE-2026-43499/](https://rootme.wssllhdg.dpdns.org/lonStack/CVE-2026-43499/)
- **Method 2:** In adb shell run:  
  `cp /path/to/your/downloaded/preload.so /data/local/tmp/ && chmod 777 /data/local/tmp/preload.so && LD_PRELOAD=/data/local/tmp/preload.so /system/bin/toybox id`

## Notes
- ⚠️ **Only supports boot.img that does not need offset patching**
- If the boot.img requires offset patching, this tool cannot handle it properly — use another toolchain
- Make sure the uploaded file is named exactly `boot.img` (case-sensitive)
