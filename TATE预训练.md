
预训练模型精度
<!--
:-    左对齐
-:	  右对齐
:-:   居中对齐
 -->
|model|可行|f1|acc|备注|
|:-:|:-:|:-:|:-:|:-:|
|TATE_paper			    | |52.52|77.08|论文给定代码（TF）|
|KL + MSEloss(base)     |×|37.73|54.68|共用FF（以下都是）|
|base + pre_LN			|√|41.29|59.89|640iter|
|base + pre_LN + ff_LN  |×|37.44|55.20|-|
|base + pre_LN + out_LN |×|35.88|54.16|-|
|base + transformer     |×|22.98|52.60|-|
|TATE					|√|38.75|60.93|850iter|
|EMMR					|×|22.37|50.52|-|
|MISA					|×|22.52|51.04|-|
|KLloss					|√|39.17|58.85|单独使用FF（以下都是）150iter|
|KL + MES(base)			|√|41.25|59.89|350iter|
|base + pre_LN			|×|40.18|58.33|-|
|base + ff_LN			|×|39.01|57.29|-|
|base + pre_LN + ff_LN	|×|37.93|57.29|-|
|base + new_MHA			|×|33.71|54.68|网上找的多头注意力|
|KL + TATE				|√|43.45|63.02|620iter|
|base + TATE			|×|37.01|54.68|-|
|KL + TATE + pre_LN		|√|43.28|63.54|870iter|
|KL + TATE + ff_LN		|√|46.31|67.18|870iter|
|将mul换成+				|-|46.32|67.18|-|
|+操作之后变换维度		|-|48.95|67.70|-|
|transformer_encoder	|×|44.04|64.06|-|
|修改交互模块				|×|37.37|54.68|放在一开始|
|||||-|
|||||-|

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTU3ODc2NjY0N119
-->