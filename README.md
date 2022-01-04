# MergeSortProject


## [16,21,11,8,12,22] -> Merge Sort

  İlk olarak dizi ortadan ikiye ayrılır -> **16,21,11**  -  **8,12,22** 
  İkiye ayrılmış dizi tekrar ikiye ayrılır -> **16,21** - **11**  -  **8,12** - **22**
  Tek eleman kalıncaya kadar bu işlem devam eder. -> **16** - **21** - **11**  -  **8** - **12** - **22** 
  Bu aşamadan sonra tek elemanlar karşılaştıralarak küçükten büyüğe ikili olarak birleştirilir -> **16,21** - **11**  -  **8,12** - **22**
  Şimdi ikili olarak sıralanmış dizi diğer dizi ile karşılaştırılarak birleştirilir. 11 16'dan küçük olduğu için dizideki diğer elemandan da küçük olduğu bilinerek gereksiz karşılaştırma kullanılmaz. İkinci tarafta ise 22 ile 8 karşılaştırlır 22 büyük olduğu için 12 ile karşılaştıralak sıralama yapılmış olur. -> **11,16,21** - **8,12,22**
  3 elemanlı sıralanmış iki dizi oluşmuş olup bu iki diziyi birleştirme işleminde önce en küçük elemanlar karşılaştırılır. 8 en küçüğü olduğu için en başa yazılır. 11 ile 12 karşılaştırlır. 11 daha küçüktür ve ikinci eleman olarak yazılır. Bu karşılaştırma işleminde dizilerinin en küçükleri karşılaştırıldıkları için tüm dizi baştan aşağı karşılaştırılmamış olur ve daha hızlı sonuçlanır. -> **8,11,12,16,21,22** şeklinde dizi elde edilmiş olur. 
  
  
## Big-O gösterimi

  Dizi sürekli ikiye bölünerek tek elemanlar elde edilir. Bu tek elemanlar da karşılaştıralarak yeniden diziye dönüştürülür. Bu noktada **log(n)** defa işlem yapılır. Bunun haricinde bölünen dizinin elemanları da karşılaştırıldığı ve sonrasında birleştirildiği için **n** defa işlem yapılmış olur.
  Bunların sonucunda *n(log(n))* defa işlem yapılmış olur.
  Bunu da Big-O olarak gösterecek olursak **O(nlog(n))** şeklinde gösteriririz.
