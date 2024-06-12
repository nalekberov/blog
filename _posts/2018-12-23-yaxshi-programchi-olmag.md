---
layout: post
lang: az
title: "Yaxşı proqramçı olmaq"
---

**Bu yazı Robert L.
Read-in [How To Be a Programmer: A Short, Comprehensive, and Personal Summary](https://www.doc.ic.ac.uk/~susan/475/HowToBeAProgrammer.pdf)
kitabının dilimizə tərcüməsidir, iş davam etməkdədir, fikirləriniz bölüşməyi unutmayın.**

Yaxşı proqramçı olmaq çətin və gözəl işdir. Proqram təminatı (PT) layihəsini reallaşdırmağın ən çətin yanı proqramçının öz
kolleqaları və istifadəçiləri ilə necə davranmağıdır. Kompyuter prqramı yazmaq çox mühimdir, yaxşı intellekt və
qabiliyyət tələb edir.

&nbsp;&nbsp;&nbsp;&nbsp;Kompyuter proqramlaşdırması adətən kurslarda tədris olunur. Ən yaxşı kitablara "The Pragmatic Programmer", "Code Complete", "Rapid
Development" və "Extreme Programming Explained" aid etmək olar. Bu kitablardam kompyuter proqramlaşdırmasını və yaxşı proqramçı olmağın çətinliklərini
öyrənmək olar. Paul Graham və Eric Raymondun esseyləri bu məqaləni oxumamışdan əvvəl oxunması tövsiyyə olunur. Bu esse   isə digər mükəmməl
işlərdən proqramlaşdırmada sosial problemləri və ən önəmli qabiliyyətləri önə çəkməklə fərqlənir.

&nbsp;&nbsp;&nbsp;&nbsp;Bu çox subyektivdir. Bu esse ona görə də daha çox şəxsi baxışlara əsaslanır. Mən özümü bir proqramçının rastlaşdığı
əksər problemlərlə sərhədləyirəm. Bu problemlərin çoxu və onların həlləri insan təbiətinə çox ümumidir. Buna baxmayaraq
bu kitabın faydalı olacağını düşünürəm. Mən bunları maksimum şüurlu toplamağa çalışmışam, hansı ki, arzu edərdim kimsə
bunu mənə 21 yaşımda olarkən izah edərdi.

&nbsp;&nbsp;&nbsp;&nbsp;Bu kitabda *boss* layihəni sizə verən hər hansı bir insanı təsvir edir. Mən *biznes*, *şirkət* və *cəmiyyət* sözlərini sinonim olaraq
istifadə edirəm, bununla bərabər, biznes pul qazanmanı, şirkət modern iş mühitini mümkün edir, cəmiyyət
isə loyallığı paylaşdığınız insanlardır.

&nbsp;&nbsp;&nbsp;&nbsp;Cəmiyyətə xoş gəldiniz.

### **Hissə 1**

# **Yeni başlayan**

## **2 Şəxsi qabiliyyətlər**

#### **2.1 Debug etməyi öyrən**

Debug etmək proqramçı olmağın təməl daşıdır. Onun birinci mənası proqramdan xətanı aradan götürmək, əsas mənası isə
*proqramı icra edərək onu izləməkdir*. Proqramı effektiv olaraq debug edə bilməyən proqramçı kordur.

İdealistlər düşünə bilərlər ki, dizayn, analiz və komplekslik teoriyasi və ya digər başqa nüanslar daha fundamentaldır,
onlar isə işsahibi proqramçılar deyildirlər. İşləyən proqramşı ideal dünyada yaşamır. Hətta o ideal olsa belə, o, böyük PT şirkətləri, GNU kimi təşkilatlar və
kolleqaları tərəfindən yazılan kodlarla işləyir və bunlarla əməkdaşlıqda olmaq məcburiyyətindədir. Bu koların çoxu mükəmməl deyildir və
mükəmməl şəkildə dokumentasiya olunmamışdır. Bu kodun necə icra olunmasından xəbərsiz olanı isə balaca bir xəta kənara
ata bilər. Çox vaxt bundan xəbərdar olmaq üçün eksperiment etmək - debug etmək lazımdır.

Debug etmək programın icrası ilə bağlıdır, proqramın özü ilə deyil. Əgər siz böyük PT şirkətindən proqram
alırsınızsa, əksər hallarda proqramı (kodunu) görmək imkanına sahib olmursunuz. Amma bəzən elə hallar olur ki, proqram
dokumentasiyada yazıldığı kimi işləmir (maşınınızı kreş etmək ağıla gələn misallardan biri olar), bəzən isə
dokumentasiya ümumiyyətlə bu barədə heç nə izah etmir. Bir çox hallarda proqramçı bir xəta yaradır, koda baxış keçirir,
amma xətanın necə baş verəcəyini təsəvvür etmir. Qaçınılmazdır ki, təxminləri tam olaraq düzgün deyil və ya elə şərt baş
verir ki, o əvvəlcədən qarşısını ala bilmir. Bəzən koda sadəcə baxış keçirmək yarayır. İşə yaramayanda isə o debug
etməlidir bunu görmək üçün.

Proqramın necə icra olunması barədə təsəvvür yaranması üçün kodu icra etmək və onu izləmək lazım gəlir. Bəzən bu
görünəndir, ekranda görünən hər hansı bir obyekt və ya iki hadisə arasında olan müəyyən gecikmə kimi. Bir çox digər
hallarda isə bu görünmür, bir verilənin koddakı vəziyyəti, hansı sətrin icra olunması və ya kompleks bir verilənlər
sturkturasında görülən iş kimi. Bu görünməz şeylər isə günüzünə çıxmalıdır.

İcra olunan proqramın daxili aləmini göstərməyin əsas yollarını belə kateqoriyalaşdıra bilərik

- Debug alətindən istifadə etmək,
- Sətrin çapolunması - proqramda müvəqqəti dəyişikliklər edərək, əsasən müəyyən informasiyanı çap edən sətr əlavə etmək
- Loglamaq - Proqrama bütün icra vaxtı ərzində log yazma imkanı əlavə etmək

Debug alətləri işləyə biən zaman həqiqətən möhtəşəmdir. Digər iki metod isə daha da əhəmiyyətlidir. Debug alətləri
bəzən dilin inkişaf prosesindən geridə qalır, və beləcə bəzən onlar işə yaramırlar. Debug aləti proqramın necə icra
olunacağını müəyyən qədər dəyişə biləcəyi üçün bütün hallarda praktiki olmaya bilərlər. Nəhayət, debug etməyin bəzi
başqa metodları da vardır, kompleks verilən strukturasını yoxlamaq kimi. Debug alətini stabil olduğu müddətcə necə
istifadə etməyi bilmək yaxşıdır. Amma digər iki metodu tətbiq etmək çox mühümdür.

Bəzi yeni başlayanların debug etməklər bağlı kodu dəyişib və icra etməklə əlaqədar şüuraltı qorxuları var. Bu başa
düşüləndir, daha çox kəşf cərrahiyəsi kimi görünür. Amma yeni başlayanlar koda onu hərəkətə gətirmək üçün barmaq etməyi
öyrənməlidir. Kodla eksperiment etməyi və edilən heç nəyin onu pis etməyəcəyindən əmin olmalıdırlar. Əgər siz müəllim və ya
mentorsunuzsa bu cür yeni başlayanlara bu prosesi izah edərək bu qorxuya qalib gəlməkdə kömək edin, yeri gələndə
əllərindən tutun. Bəzi yeni başlayanlar başlanğıcda yaranan qorxuya görə yolu yarıda qoyurlar.
