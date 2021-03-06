# keytext4py
**KEY TEXT** Extractor for **PY**thon


## Get Isolated Python Runtime (If Needed)
```sh
wget -qO - https://ghproxy.com/https://raw.githubusercontent.com/innerNULL/pypack/main/pypack.sh | bash /dev/stdin pypack.json
cd _build && mkdir _pyenv && cd _pyenv && tar -xvzf ../pyenv.tar.gz && cd ../../
ln -s ./_build/_pyenv/bin/python ./python
```
or any other approachs.


## Benchmarking
```sh
mkdir build && cd build
cmake ../ -DKEYTEXT4PY_BENCHMARKING=TRUE
./benchmarks/cpp/benchmarking
```

## Install
```bash
python -m pip install ./ -vvv
# or
python -m pip install https://github.com/innerNULL/keytext4py/archive/refs/heads/main.zip -vvv
```


## Run Examples
### Chinese
```bash
python demos/zh_fast_keywords_extraction_v0.py
python demos/zh_fast_keywords_extraction.py
```
The results is: 
```
text:
https://zh.wikipedia.org/wiki/%E
5%A6%87%E4%BA%BA%E7%94%BB%E5%83%
8F  妇人画像》（英语：Portrait of a Lady）
是尼德兰画家罗希尔·范德魏登的小型橡木板油画，估计在1460年左
右完成。画中女子面纱、领口、脸部和手臂线条形成几何图形，头饰和面
部由光线从上向下照亮，共同组成画面构图。模特儿的美几乎有些不自然
，呈现哥特式的优雅，画上黑暗与光明的鲜明对比又令这种美和优雅更为
显著。  范德魏登因善于在画作中入木三分地刻画人物性格获后代画家
高度评价，他的晚年一直忙于创作肖像画[1]。以《妇人画像》为例，
画中人体格瘦弱、双眼视角下垂，手指紧紧绞在一起，表现出谦卑和内敛
的气质[2]。对于人物苗条的身材，画家通过哥特式拉长理念呈现，如
狭窄的双肩、扎紧的头发、光亮的额头，以及头饰构成的精致框架。《妇
人画像》是唯一有范德魏登签名且普遍认可是他创作的女子画像[1]，
由于缺乏注明，模特儿的身份暂无定论。  范德魏登不坚持将人物理想
化，但一般还是会把肖像画得更加讨喜。他笔下的模特儿往往身着非常时
髦的服装，面部特征圆滑，甚至接近雕塑效果，有些已经显得不自然。适
...

key-words:
      范德魏登: 14.285714149475098
        人物: 11.428571701049805
        面纱: 11.428571701049805
        女子: 10.0
        妇人: 10.0
        画像: 10.0
        画家: 10.0
        背景: 8.571428298950195
        头饰: 8.571428298950195
        耳朵: 5.714285850524902
```
