## Go ilə irəli ...

İlk öncə mühəndislərə salam :)

*Bu bloqun əsas məqsədi 5-10 dəqiqə ərzində oxuna biləcək proqram sistemləri mühəndisliyi sahəsində özüm üçün maraqlı maraqlı hesab etdiyim yazıların dərc olunmasıdır. Hesab edirəm ki, 5-10 dəqiqə bir fikri çatdırmaq üçün kifayət qədər yetərli zamandır.*

Bloqun ilk yazısı Go dilinə həsr olunur. Mətn konseptual xarakterlidir və proqramlaşdırma dilinin praktiki realizasiyasını əhatə etmir. Yazı Golang dili haqqında ümumi məlumat almaq istəyənlər üçün maraqlı ola bilər. Mən özüm də həm iş şəraitində, həm də layihələrdə bu proqramlaşdırma dilindən istifadə edirəm. İlk öncə bildirmək istərdim ki, proqramlaşdırma sahəsində proqramlaşdırma dilləri 2 qrupa bölünür: pis dillər və istifadə olunmayan dillər. Go proqramlaşdırma dili də Python, C, Java, C++, C#, Visual Basic, Javascript, Assembler, SQL, Pascal kimi pis dillər qrupuna daxildir :)


##### **Giriş**
Go proqramlaşdırma dili (alternativ və daha çox istifadə olunan adı Golang) - in başlanğıcı 2007-ci il kimi qəbul edilir. 2012-ci ildə Google şirkəti tərəfindən ictimaiyyətə açıq edilmişdir.

Rəsmi səhifə: [rəsmi səhifə](https://go.dev/)
Mənbə kodları: [github.com](https://github.com/golang/go)

*GO! dili ilə qarışıq salmaq olmaz*, bu tamam ayrı bir proqramlaşdırma dilidir, yaradıcılarının Google ilə [ad üstündə](https://github.com/golang/go/issues/9) mübahisələri uzun müddət davam etmişdir.

##### **Əsas tətbiq sahələri**
Golang-in bir sıra tətbiq sahələri olduğuna baxmayaraq, əsas tətbiq sahələri aşağıdakılardır:
- Bulud texnologiyalarına yönümlü sistemlər
- Serverdə icra olunan proqram təminatları
- Terminal tipli proqram təminatları (mütəxəssislər tərəfindən daha çox CLI - Command Line Interfaces) kimi tanınır
- Veb sistemlər
- DevOps və Production mühitlərinin idarəolunması sistemləri
- Suni intelekt (AI) və Data Science sahəsində 
- Mikrokontroller, robot sənayesində də istifadə edənlər var

Golang üzrə ən məşhur layihələrin bəziləri Kubernetes, Docker, Helm, Terraform. Bütün [siyahı](https://github.com/golang/go/wiki/Projects) ilə tanış olmaq mümkündür. 


#### **Golang -in yaranma motivasiyası**

Google şirkəti bir müddət sonra çatmaq istədiyi nəticələrə mövcud üsul və proqramlaşdırma dilləri ilə çatmağın səmərəsiz olduğunu başa düşdü. Bu səbəbdən də, Go dili təzə proqramlaşdırma dili yazılsın deyə hazırlanmadı, bir sıra problemləri aradan qaldırmaq üçün dizayn edilmiş dildir.

Golang dilinin yaradıcılarından biri olan [Rob Pike](https://evrone.com/rob-pike-interview) dən sitat:
> Go layihəsinin məqsədləri Google-da proqram təminatlarının yazılması prosesində çətinliklərin və prosesin yavaşlığının qarşısını almaq idi. Və eyni zamanda prosesin özünü daha məhsuldar və miqyaslı hala gətirilməsi məqsəd idi. Bu dil böyük sistemləri yazan, dəstəkləyən və düzənləyən şəxslər tərəfindən hazırlanmışdır.

Go dilinin hazırlanmasında C, Pascal, Modula, Oberon dilinin müsbət realizə komponentləri baza qismində götürülmüşdür. Python, C++, Java və s. dillərindən də müsbət hissələr dilə təsir etmişdir.

Yekunda Golang sürətli proqramlaşdırıla bilinən, kompüterin processor nüvələrindən effektiv istifadə edə bilən və kompüter şəbəkəsi üzərindən işlənilməsi düşünülən proqram təminatlarının hazırlanmasında istifadə oluna biləcək effektiv və müasir proqramlaşdırma dilidir.

#### Golang -in əsas xarakterik xüsusiyyətləri
   
- sadə və təmiz sintaksis, proqramlaşdırma kodunu oxunaqlı və rahat təhlil oluna biləcək edir;
- dəyişən tipləri ciddi statikdir, dolayısı ilə kompilyasiya zamanı statik səhvlərin qarşısını alır və digər tərəfdən də icra və build prosesini sürətləndirir. Build prosesi dedikdə, proqramı mühitdə icra olunması üçün paketlənməsi prosesi nəzərdə tutulur.
- Garbage collector (operativ yaddaşda "zibillərdən azad olunma") mövcuddur. Çox effektivdir, operativ yaddaşda elementlərə əlçatanlığı və istifadəni təhlükəsiz edir, eyni zamanda proqram təminatının icrası kompüter resurslarının istifadəsini effektiv edir.
- sintaksis eyniliyi - kodu minimal, dəqiq və başa düşülən edir. Go dilində bir problemin icrasının yalnız bir üsulu mövcuddur və həmin üsuldan istifadənin də qaydası bir cürdür. Məsələn, dövrlərdən istifadə olunamsı üçün yalnız [for](https://go.dev/tour/flowcontrol/1) konstruksiyasından istifadə oluna bilir. Bu xüsusiyyət proqramlaşdırma prosesini sürətləndirir.
- Obyekt yönümlü proqramlaşdırmanın məlum ümumi prinsiplərinin olmaması
- Try-catch operatorunun olmaması, əvəzində icra olunmuş metodun nəticəsini üzərindən çıxışlar icra olunur

Golang-in əsas kitabxanası məhdud funksiyalıdır. Əlavə funksiyalar üçün kitabxanaların əlavə olunmasına ehtiyac duyulur. Başqa proqramlaşdırma dilindən Golang -a keçid edən şəxslər, öncəki proqramlaşdırma dillərində istifadə olunan metod və üsulların da bu dilin tərkibinə qatılmağını arzu edirlər. Lakin Golang yaradıcıları dilin əsas yaranma prinsiplərinə sadiq qalaraq, yeni növ funksiyaların əlavə edilməsində  konservativ yanaşmanı tətbiq edirlər. Çünki hamı tərəfindən istifadə olunmayan metodların dilə əlavə olunması onun proqram təminatı məhsullarının kodlarının icra effektivliyini aşağı salır. Dolayısı ilə, proqramçı hansı sa metod və funksiyanın icrasını öz layihəsində özü realizasiya etməlidir. Golang dilinin gözəlliyi və unikallığı onun kompakt və birmənalı sintaksisinin olmasındadır.

#### Golang asandır və eyni zamanda çətindir

Sintaksis minimallığı onu ilk baxışdan asan dil kimi göstərir. Lakin, Go-nun daxili mexanizmləri və realizasiyası çox qəlizdir. Rob Pike özü belə deyir:
> Go dili mənim işlədiyim layihələrin içində ən qəlizidir. Bu uzun bir layihələndirmə, düşünmə, əziyyət və dürüstləşmələr tələb etdi. Sadəlik, qəlizliyi gizlətmək sənətidir. 

Go dilində "sadəliyi" təmin edən komponentlər:
- **Garbage Collector** - Bu go dilinin ən sadə funksiyasıdır. Onun icra interfeysi yoxdur, özü hər şeyi avtopilot rejimdə edir. Amma bu dilin ən qəliz komponenti hesab olunur. Çünki "zibil idarəedilməsi" operativ yaddaşda element adresslərinin təhlükəsizliyini təmin etməklə yanaşı, proqram təminatlarının sürətli icra edir və eyni zamanda kompüter resurslarının effektiv idarəedilməsini təmin edir.
- **Paralelləşmə və ya GoRoutine** - parallelləşmə modelinin sadə və birbaşa icrası. Yeni alt prosesin yaradılması o qədər asandır ki, ilk baxışdan sanki siz heç bir şey belə etməmisiz. Digər proqramlaşdırma dillərində bunu etmək üçün ciddi mexanizmlərdən istifadə etmək lazımdır.
- **İnterfeyslər **- yaradıcıların unikal dizayn həlli, OOP(Obyekt yönümlü proqramlaşdırma) tərəfdarlarının kritikalarının böyük hissəsinə cavab verir. 
- **Paketlər ** - Digər dillərin kitabxana idarəetməsinə nisbətdə və müqayisədə sürprizsiz işləyir, proektə qoşursan və işlədirsən. Go get komandası köməyi ilə, paketləri istənilən yerdən çağırmaq mümkündür - Gopkg, GitHub, GitLab, BitBucket və öz mənbə kodu repositoriyanızdan.
- **Standart kitabxanalar** - Go standart kitabxanaları bir çox rahat funksiyaları təşkil edir, bu da dilin çox funksiyalı olduğunu göstərir. Sadə *import "net/http"* çağırmaqla, siz artıq proqramınızın daxilində veb-server komponentini bütün funsiyaları ilə birlikdə əldə etmiş olursuz.

##### **Təklif olunan istifadə sahələri**
Bir qədər Go dili haqqında təsəvvürünüzün olduğuna inanıram. Onun istifadəsinin sadə olduğunu və məhsuldar olduğunu istehsalat təcrübəsində artıq sübut olunub. Lakin sual çıxır, hansı sahələrdə o ekkeftivdir:

C# və Java kimi dillərlə müqayisə düzgün olmasa da, müqayisə etməyə çalışsaq, onlarlın faktiki bazar tutumu ilə müqayisə etmək çox çətindir. Çünki bu dillər biznesin bir sıra sahələrinin avtomatlaşdırılmasında yaxından iştirak edir. Əlisndə Go dilinin C# və Java kimi ümumi təyinatlı proqram dillərini əvəz etmək kimi bir planı da yox idi, çünki Go dili yüksəksürətli kompüter şəbəkələri və effektiv proqram sistemləri dili kimi çıxış edilməsi üçün dizayn edilmişdi, geniş təyinatlı proqramlaşdırma dili üçün nəzərdə tutulmamışdı.

Lakin Go dili geniş kütləyə açılandan sonra, proqrammistlər tərəfindən digər sahələrin də avtomatlaşdırılmasında istifadəsi təmin edildi və effektivliyi görüldü.

Go dilini müqayisə etmək gərəkirsə, onu C/C++, Rust kimi dillərlə müqayisə etmək daha doğru olardı. Çünki onlar da Statik sərt tiplərlə işləyən və kompile olunan dillər qrupuna aiddir.

Go dili bü gün də inkişaf edir. Yeni sahələrdə tətbiqi genişlənir, paketlər, frameworklər hazırlanır. Effektivliyi görüldükdən sonra bir sıra şirkətlərdə artıq əsas dil kimi çıxış edir.

Go dilində bir məhsulu production mühitinə çıxan proqramçılar, növbəti məhsulunu məhs Go dilində yazmağı arzulayır.

###### Praktiki tətbiq sahələri üzrə məşhur kitabxanalar:

- Bulud texnologiyalı veb-servizlər, xüsusi ilə mikroservizlərin hazırlanması -kitabxanalar Go kit, Micro, Gizmo, Kite, Goa, Caddy;
- REST API lərin hazırlanması - kitabxanalar Gin, Martini, Revel, Gorilla, Beego, Fiber;
- RPC API lərin hazırlanması - kitabxanalar RPC, Twirp, Spiral, Gorilla;
- GraphQL API - lərin hazırlanması - kitabxanalar graphql-go, gqlgen, thunder;
- Serverless funksiyaların hazırlanması - Google Cloud Functions, Sparta, Gordon;
- WebAssemply texnologiyası üzrə veb-interfeyslərin hazırlanması - Hugo, Vugu, TinyGo, Vecty;
- Robototexnika, IoT və bort sistemləri - Gobot, Mainflux, TinyGo, EMBD;
- CLI proqramlar - с помощью Cobra, cli;
- Maşın öyrənilməsi və suni intelekt sistemləri - GoLearn, Gorgonia.

Bir sıra qeyri-adi cəhdlər:

- mobil proqramların hazırlanması - gomobile;
- Desktop proqramların hazırlanması -  lorca, Wails, Fyne;
- oyun proqramlarının hazırlanması - Ebiten, Pixel, G3N;
- çat botlarının hazırlanması Discord, Telegram, Slack və s.;
- Smart kontrakt və blokçeyn texnologiyaları.

Müxtəlif tətbiq sahələrinə və ekspermentlərə baxmayaraq ən çox tətbiq olunan sahələr - bulud texnologiyaları, veb və sistem proqramlaşdırması kimi müəyyənləşdirmək olar. Amma fərqli proqramçıların düşüncələri və əməkləri bu sərhədləri aşır, Go dilinə yeni tətbiq sahələri qatır.

##### **Yekun**
Bu dili öyrənmək istənilən halda proqramçıya yeni imkanlar tanıdır və bir sıra tapşırıqların effektiv icrasını təmin edir. Digər tərəfdən də, İT məsələlərin həllində fərqli bucaq tanıdır. İlk proqramlaşdırma dili kimi öyrənilməsi sintaksisin sadəliyi baxımından mümkündür, sadəcə tətbiq sahəsində ilk zamanlarda bir qədər səbr və dözümlülük tələb edə bilir. Digər dillərdən keçid edənlər üçün isə, xüsusi ilə Obyekt yönümlü proqramlaşdırma yanaşması ilə proqramlaşdıranlar üçün dilin konstruksiyası bir qədər dolaşıq gələ bilər, amma bir müddət sonra həm öyrəşilir, digər tərəfdən də, bir sıra məsələlərin həllində Obyekt yönümlü yanaşmağın zəruri olmadığı aşkarlanır. 
İstənilə halda, cəhd etməyə dəyər. Xüsusən də, Backend proqramçılar və sistem proqramlaşdırıcıları üçün daha effektiv olacağını düşünürəm.
Bu mətnə öz fikirlərinizi bildirməyiniz, mətnin daha keyfiyyətli olmağına töhvə verəcəyinə inanıram. Eyni zamanda termin tərcümələrində də müzakirələrə açığam.
Növbəti zamanlarda, Go ilə proqramlaşdırma üzrə praktiki yazıların dərc olacağını da planlayıram.
Uğurlar hər kəsə.

***İstinad linkləri***

1. [Go dilinin rəsmi səhifəsi](https://go.dev/)
2. [Go wiki səhifəsi](https://en.wikipedia.org/wiki/Go_(programming_language))
3. [Go dilini xüsusi edən nədir?](https://tproger.ru/translations/chto-delaet-go-takim-neobychnym/)
4. [Go dilinə ilk addımlar](https://docs.microsoft.com/en-us/learn/paths/go-first-steps/)



