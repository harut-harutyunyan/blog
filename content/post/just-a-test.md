---
title: "Just a Test"
subtitle: Each post also has a subtitle
date: 2022-09-24T03:03:50+04:00
tags: ["example", "markdown"]
# draft: true
---

You can write regular [markdown](http://markdowntutorial.com/) here and [Hugo](https://gohugo.io) will automatically convert it to a nice webpage.  I strongly encourage you to [take 5 minutes to learn how to write in markdown](http://markdowntutorial.com/) - it'll teach you how to transform regular text into bold/italics/headings/tables/etc.

**Here is some bold text**

## Here is a secondary heading

Here's a useless table:
 
| Number | Next number | Previous number |
| :------ |:--- | :--- |
| Five | Six | Four |
| Ten | Eleven | Nine |
| Seven | Eight | Six |
| Two | Three | One |
 

How about a yummy crepe?

![Crepe](http://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg)

Here's a code chunk with syntax highlighting:

```python
    @classmethod
    def collect_light_info(cls):
        this_node = cls.this_node()

        vals = ["mute", "intens", "exp", "col"]

        knobs = [i for i, n in this_node.knobs().items() if i.startswith("lgt_") and i.rsplit("_", 1)[1] in vals]
        light_info = {l.replace("lgt_", "").rsplit("_", 1)[0]:{} for l in knobs}
        for k in knobs:
            lgt_name = k.replace("lgt_", "")
            lgt_name, val = lgt_name.rsplit("_", 1)
            light_info[lgt_name][val] = this_node[k].getValue()

        return light_info
```