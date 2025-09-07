# xiaozhi_2.0.0
# 1. Mở ESP-IDF Command Prompt
'' cd D:\Espressif\frameworks\esp-idf-v5.5\xiaozhi_2.0.0
idf.py fullclean'' 


python -m esptool --chip esp32s3 --port COM4 --baud 921600 read_flash 0x800000 0x1000 models_read.bin
# 3. idf.py build
# 4. idf.py -p COM4 flash
# 5. idf.py -p COM4 monitor
# Xoa trong essp
python -m esptool --chip esp32s3 --port COM4 --baud 921600 erase_flash
   Flash models:
idf.py -p COM4 write-flash 0x800000 models/srmodels.bin
Monitor logs:
 idf.py -p COM4 monitor
