---
layout: post
title:  "Image in Post"
date:   2014-12-10
---
>Start to learn the zettlekasten knowledge management system, which utilize zotero and obsidian to establish a routine workflow. I had a hard time switching from Mendeley to Zotero. As a convinent knowledge management software, Mendeley is easy to use, has an easy access to Elsevier database, and has powerful fuzzy search ability. Since I brought a new laptop and will go through a tough data transfer process, I forced myself to learn something new.>

Zotero has a lot of powerful add-ons. As always mentioned in [forum](https://forums.zotero.org/discussion/40967/zotfile-annotation-color-extraction/p1) that using zotfile can extract notes seperated by colors, I really did not understand how to change the hidden option labeled "pdfExtractions.colorNotes" as described in [Zotfile's own page](http://zotfile.com/). I tried a whole noon and finally found that [Zplusless’s blog](https://blog.monsterz.cn/blog/zotero%E4%B8%ADzotfile%E6%8F%90%E5%8F%96%E7%AC%94%E8%AE%B0%E6%A0%BC%E5%BC%8F%E8%AE%BE%E7%BD%AE/) saved my ass.


Edit—->Preferences—->Advanced—->Config Editor—->search "zotfile.pdfExtraction"

Firstly, click **extensions.zotfile.pdfExtraction.colorAnnotations** and change value from **False** to **True**.
Secondly, change the parameters in **highlight, note and underline** . You can refer to the setting parameters mentioned in [forum](https://forum.obsidian.md/t/zotero-best-practices/164/57) or change things you want.
```
extensions.zotfile.pdfExtraction.formatAnnotationHighlight => <p>"%(content)" (%(cite)) (%(label); p.%(page); %(color_category)/%(color); %(uri))</p>
extensions.zotfile.pdfExtraction.formatAnnotationNote => <p><i>%(content) (<a href="%(uri)">note on p.%(page)</a>) (%(label); p.%(page); %(uri))</p><br>
extensions.zotfile.pdfExtraction.formatAnnotationUnderline => <p>"<u>%(content)</u>" (%(label); p.%(page); %(uri))</p>
```
After being exported, results in a note like this:
![image.png](https://upload-images.jianshu.io/upload_images/31743-e1503d97020f7a58.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


