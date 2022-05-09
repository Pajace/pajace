1. 使用 unzip 將 epub 解壓縮

```
unzip yourEbooks.epub
```

2. 使用 opencc 將簡體轉成繁體

```
opencc -i inputSCfile.txt -o outputTCfile.txt
```

3. 將所有檔案再度打包回 epub

Linux

```
zip -rX "../$(basename "$(realpath .)").epub" mimetype $(ls|xargs echo|sed 's/mimetype//g')

```

Mac

```
zip -rX "../myprecious.epub" mimetype $(ls|xargs echo|sed 's/mimetype//g') -x *.DS_Store

```
