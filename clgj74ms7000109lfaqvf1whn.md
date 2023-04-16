---
title: "Ubuntu əməliyyat sistemlərinin yenilənməsi strategiyası"
datePublished: Sun Apr 16 2023 09:19:54 GMT+0000 (Coordinated Universal Time)
cuid: clgj74ms7000109lfaqvf1whn
slug: ubuntu-emeliyyat-sistemlerinin-yenilenmesi-strategiyasi
tags: ubuntu, linux, canonical, ubuntu-1804

---

Ubuntu əməliyyat sistemi bir çox şəxsin Linux əməliyyat sistemlərinə keçid etməsində rol oynayıb. Hal-hazırda Big Data və Machine Learning üçün modellərin proqramlaşdırılması və PaaS sistemlərin (Databricks, HDInsight və s) əməliyyat sistemi kimi Ubuntu əməliyyat sistemlərini istifadə edir. Digər tərəfdən, program təminatı istehsalçıları öz sistemlərini Ubuntu sistemində testdən keçirir. Bu da Ubuntu əməliyyat sisteminin cəlb ediciliyini artırır.  
Böyük şirkətlər (AWS, Google, Microsoft) öz sənədləşmə işlərində Ubuntu əməliyyat sisteminin xüsusiyyətlərini nəzərə alır.

Ubuntu ilə yanaşı Debian, RHEL, SUSE sistemləri də ən çox istifadə olunan və dəstək göstərilən, istifadəçi təcrübəsi olan sistemlərdir ki, yeni layihələrdə server və informasiya sistemləri qurulanda əsasən spesifikasiyaları nəzərə alaraq qeyd olunan əməliyyat sistemlərinə müraciət olunur.

Təbii ki, digər Linux tipli əməliyyat sistemləri də vardır, lakin onların istifadəsində bəlli riksləri istifadəçi tərəf öz üzərinə götürür.

Məqalənin yazılmasına aydınlıq gətirmək üçün, bir az ümumiləşdirilmiş giriş informasiyasının verilməsinə ehtiyyac yaranır. Məsələ burasıdadır ki, qeyd olunan əməliyyat sistemləri bəlli müddətdən sonra versiyası üzrə yaşam dövrünü bitirir. EOL (End Of Life) kimi adlandırılan məqam Ubuntu 18.04 LTS versiyası üçün artıq qapıdadır. 5 il dəstək müddəti artıq bitmək üzrədir. [Ətraflı xarici keçid](https://ubuntu.com/blog/ubuntu-18-04-eol-for-devices). Qısacası, EOL dan sonra nə olacaq?

* Canonical şirkəti təhlükəsizlik təkmilləşdirmələri etməyəcək, nəticə olaraq sistemlərin istismarı riksli vəziyyət alacaq
    
* Digər proqram təminatı istehsalçıları öz proqramlarını EOL müddəti başa çatmış sistemlərdə sınaqdan keçirmir. Deyək ki, Jenkinsin təzə versiyası çıxıb, lakin siz EOL müddətli sistem işlədirsiz, Jenkins proqramçıları həmən mühitdə test eləmədikləri üçün sistemin istənilən kimi işləmiyə bilir. Təbii istisna hal olaraq, bəxdəbəxt bəlli müddət işləyə bilər, lakin ciddi layihələrdə bu cürə riskin alınması məsləhət edilən üsul sayılmaz.
    
* Oturuşmuş İT şirkətlərdə kompüter təhlükəsizliyi şöbəsinin əməkdaşları bu sistemlərin söndürüləcəyi barədə bildirişlər və ya əməli fəaliyyətə keçə bilir. Nəticədə keçid prosesi öncədən planlamalıdır.
    

Reallıqda bəzən olur ki, hər-hansı səbəbdən yenilənmə texniki cəhətdən mümkün olmur, bunun üçün Canonical şirkəti [ESM (Expanded Security Maintenance)](https://ubuntu.com/security/esm) təklif edir. Bununla bəlli ödəniş həyata keçirərək siz sistemə yalnız təhlükəsizlik ilə bağlı yenilikləri tətbiq edə bilərsiniz. Bir sözlə, artıq istismara verilmiş, içərisinidə heç bir dinamik dəyişiklik olmayacaq sistemlər üçün əlverişli seçimdir. Əl vurma onsuzda işləyir prinsipi ilə baxsaq, daha 5 il müddətinə təhlükəsizlik ilə bağlı yeniliklərdən faydalana bilərsiz.