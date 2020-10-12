# *MISC WRITEUP ISITDTU 2020*
>  ## iphoneX.png  

* [Link download Challange](https://drive.google.com/file/d/1-etAvBWVNr0SvGwBUlgNmhvwoXEFPXgL/view)

![screenshoot](https://i.imgur.com/RwP3jgK.png)



* Sau khi tải file về ta check file bằng lệnh ``` file iphoneX.png ``` 

```bash
kali@kali:~/Desktop$ file iphoneX.png
iphoneX.png: PNG image data, 333 x 250, 8-bit/color RGB, non-interlaced
```
* Sau một thời gian tìm hiểu thì bài này chúng ta cần xử lí pixel và ta có công cụ để xử lí https://github.com/csisl/appa 

   * Dùng lệnh *git clone +link* để cài tool ``` git clone https://github.com/stncal/appa.git ```

* Sau đó ta dùng lệnh ``` python3 appa/appa.py -d iphoneX.png ```

* Ta được: 

```bash
kali@kali:~/Desktop$ python3 appa/appa.py -d iphoneX.png
==> Decoding image: True

==> Pixel data
        First 3 pixels/possible text: [(212, 213, 215), (213, 212, 215), (213, 213, 214)]
        Possible text found at pixels[(213, 213, 214)]
        Possible text found at pixels[(213, 213, 214)]
        Possible text found at pixels[(212, 212, 214)]
        Possible text found at pixels[(213, 213, 214)]
        Possible text found at pixels[(212, 212, 214)]
        Possible text found at pixels[(212, 213, 214)]
        Possible text found at pixels[(213, 213, 214)]
        Possible text found at pixels[(213, 213, 214)]
        Possible text found at pixels[(212, 212, 214)]
        Possible text found at pixels[(214, 214, 216)]
        Possible text found at pixels[(213, 213, 216)]
        Possible text found at pixels[(213, 213, 216)]
        Possible text found at pixels[(214, 214, 216)]
        Possible text found at pixels[(213, 213, 216)]
        Possible text found at pixels[(213, 213, 216)]

==> Translating each pixel for possible text
        [(212, 213, 215), (213, 212, 215), (213, 213, 214), (212, 212, 215), (213, 212, 214), (213, 213, 214), (212, 211, 213), (212, 211, 213), (212, 212, 214), (212, 213, 215), (212, 212, 214), (213, 213, 214), (212, 212, 215), (213, 212, 214), (212, 212, 214), (212, 213, 215), (212, 213, 215), (212, 213, 214), (212, 212, 215), (213, 212, 214), (213, 213, 214), (212, 213, 214), (213, 213, 215), (213, 213, 214), (212, 213, 215), (213, 212, 215), (212, 212, 214), (212, 212, 215), (213, 214, 216), (214, 214, 216), (214, 213, 216), (213, 213, 215), (213, 213, 216), (214, 213, 215), (213, 214, 216), (213, 213, 216), (214, 213, 215), (213, 214, 215), (214, 214, 216), (214, 214, 215), (213, 214, 216), (213, 213, 216), (214, 213, 215), (214, 214, 215), (213, 213, 216), (214, 214, 215), (213, 214, 216), (214, 214, 215)]
        01110111 = w
        00110011 = 3
        01101100 = l
        01100011 = c
        00110000 = 0
        01101101 = m
        00110011 = 3
        01011111 = _
        01110100 = t
        00110000 = 0
        01011111 = _
        01110011 = s
        01110100 = t
        00110011 = 3
        01100111 = g
        00110000 = 0

Appa found an extremely large string in the image. To save your console, results are saved to file: iphoneX.results
String length: 16
```
* Sau khi run the command ta được file ```iphoneX.results``` open file thấy ngay flag :blush:

![screenshoot](https://i.imgur.com/5mvZMHn.png)

> ##  ISITDTU{w3lc0m3_t0_st3g0}


