GitHub ve Komutları
============
*Git, bilgisayarınızda yerel olarak gerçekleşen GitHub ile ilgili her şeyden sorumlu olan ücretsiz ve açık kaynaklı dağıtılmış sürüm kontrol sistemidir. Bu hile sayfası, kolay referans için en önemli ve yaygın olarak kullanılan Git komutlarını içerir.*

## Çevrilmiş Versiyonlar
- [İngilizce versiyonu (orijinal)](README.md)
- [Versiyon Française](READMEfr.md)
- [İspanyolca versiyonu](READMEes.md)

### KURULUM & GUIS
_Git için platforma özgü yükleyicilerle GitHub, günlük etkileşim, inceleme ve depo senkronizasyonu için grafiksel bir kullanıcı arayüzü sağlarken, komut satırı aracının en son sürümleriyle güncel kalma kolaylığı da sağlar._

#### Windows için GitHub
_https://windows.github.com_

#### Mac için GitHub
_https://mac.github.com_

_Linux ve Solaris platformları için en son sürüm resmi Git web sitesinde mevcuttur._

#### Tüm Platformlar için GitHub
_http://git-scm.com_

### KURMAK
_Tüm yerel depolar genelinde kullanılan kullanıcı bilgilerinin yapılandırılması_

| kurmak |
|-------|
|`git config --global user.name “[ad soyadı]”` <br/> Sürüm geçmişini incelerken kredi için tanımlanabilir bir ad belirleyin|
|`git config --global user.email “[geçerli e-posta]”` <br/> Her geçmiş işaretleyicisiyle ilişkilendirilecek bir e-posta adresi ayarlayın|
|`git config --global color.ui auto` <br/> Git için kolay inceleme için otomatik komut satırı renklendirmesini ayarlayın|

### KURULUM & BAŞLATMA
_Kullanıcı bilgilerini yapılandırma, depoları başlatma ve klonlama_

| Komut | Açıklama |
| ------- | ----------- |
| `git init` | Yerel bir Git reposunu başlat |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Uzak bir reponun yerel bir kopyasını oluştur |

### Temel Anlık Görüntü
_Anlık görüntüler ve Git hazırlama alanıyla çalışma_

| Komut | Açıklama |
| ------- | ----------- |
| `git status` | Durumu kontrol et |
| `git add [dosya-adı.txt]` | Hazırlama alanına bir dosya ekle |
| `git add -A` | Tüm yeni ve değiştirilen dosyaları hazırlama alanına ekleyin |
| `git commit -m "[commit message]"` | Değişiklikleri commit et (açıkla) |
| `git reset [dosya]` | Çalışma dizinindeki değişiklikleri koruyarak bir dosyayı sahneden kaldırın |
| `git diff` | Değiştirilen ama sahnelenmeyen şeyin farkı|
| `git diff --staged` | Sahnelenen ancak henüz taahhüt edilmeyen şeyin farkı |
| `git rm -r [dosya-adı.txt]` | Dosyayı (ya da dizini) sil |
| `git remote -v` | Şu anda çalışan dosyanın veya dizinin uzak deposunu görüntüleyin |

### Dallanma ve Birleşme
_Isolating work in branches, changing context, and integrating changes_

| Komut | Açıklama |
| ------- | ----------- |
| `git branch` | Bracnh'leri listeleyin (yıldız işareti mevcut branch'i gösterir) |
| `git branch -a` | Tüm brach'leri listele (yerel ve uzak) |
| `git branch [şube adı]` | Yeni bir branch oluştur |
| `git branch -d [şube adı]` | Branch'i sil |
| `git push origin --delete [şube adı]` | Uzak branch'i sil |
| `git checkout -b [şube adı]` | Yeni bir branch oluştur ve ona geçiş yap |
| `git checkout -b [şube adı] origin/[şube adı]` | Uzak branch'i klonla ve ona geçiş yap |
| `git branch -m [eski şube adı] [yeni şube adı]` | Yerel branch'i yeniden adlandır |
| `git checkout [şube adı]` | Belirtilen branch'e geçiş yap |
| `git checkout -` | Son kontrol edilen branch'e geç |
| `git checkout -- [file-name.txt]` | Bir dosyadaki değişiklikleri sil |
| `git merge [şube adı]` | Bir branch'i aktif branch ile birleştir |
| `git merge [kaynak dalı] [hedef şube]` | Branch'i hedef branch ile birleştir |
| `git stash` | Yarım kalan bir çalışma dizinindeki değişiklikleri saklayın |
| `git stash clear` | Saklanan tüm girişleri kaldır |
| `git stash pop` | En son stash'i çalışma dizinine uygula |
| `git log` | Mevcut dalın geçmişindeki tüm commitleri göster |

### Projeleri Paylaşma ve Güncelleme
_Başka bir depodan güncellemeleri alma ve yerel depoları güncelleme_

| Komut | Açıklama |
| ------- | ----------- |
| `git push origin [şube adı]` | Uzak repoya bir branch gönder |
| `git push -u origin [şube adı]` | Değişiklikleri uzak repoya aktarın (ve branch'i hatırla) |
| `git push` | Değişiklikleri uzak repoya aktarın (ve branch'i hatırla) |
| `git push origin --delete [şube adı]` | Uzak branch'i sil |
| `git pull` | Yerel repoyu en yeni commit'e güncelleyin |
| `git pull origin [şube adı]` | Değişiklikleri uzak repodan çek |
| `git remote add origin ssh://git@github.com/[kullanıcı adı]/[depo-adı].git` | Uzak repo ekle |
| `git remote set-url origin ssh://git@github.com/[kullanıcı adı]/[depo-adı].git` | Bir reponun başlangıç branch'ini SSH olarak ayarla |
| `git fetch [alias]` | Git uzak sunucusundan tüm dalları al |

### İnceleme ve Karşılaştırma
_Günlükleri, farkları ve nesne bilgilerini inceleme_

| Komut | Açıklama |
| ------- | ----------- |
| `git log` | Değişiklikleri görüntüle |
| `git log --summary` | Değişiklikleri görüntüle (detaylı) |
| `git log --oneline` | Değişiklikleri görüntüle (kısaca) |
| `git diff [source branch] [hedef şube]` | Birleştirmeden önce değişiklikleri önizle |
| `git log branchB..branchA` | BranchA'da olup BranchB'de olmayan commitleri göster |
| `git log --follow [dosya]` | Dosyayı değiştiren commit'leri, yeniden adlandırmalarda bile göster |
| `git diff branchB...branchA` | BranchA'da olup BranchB'de olmayanın farkını göster |
| `git show [SHA]` | Git'te herhangi bir nesneyi insan tarafından okunabilir biçimde göster |

### TRACKING PATH CHANGES
_Sürüm dosyası kaldırılır ve yol değişiklikleri yapılır_

| Komut | Açıklama |
| ------- | ----------- |
| `git rm [dosya]` | Dosyayı projeden silin ve kaldırma işlemini commit için aşamalandırın |
| `git mv [mevcut-yol] [yeni-yol]` | Mevcut bir dosya yolunu değiştirin ve taşımayı aşamalandırın |
| `git log --stat -M` | Taşınan tüm yolların göstergesiyle birlikte tüm commit günlüklerini göster |

### REWRITE HISTORY
_Dalları yeniden yazma, commit'leri güncelleme ve geçmişi temizleme_

| Komut | Açıklama |
| ------- | ----------- |
| `git rebase [branch]` | Mevcut dalın herhangi bir commit'ini belirtilenden önce uygula |
| `git reset --hard [commit]` | Sahneleme alanını temizle, çalışma ağacını belirtilen commit'ten yeniden yaz |

### IGNORING PATTERNS
_Dosyaların istenmeden sahnelenmesini veya işlenmesini önleme_

| Komut | Açıklama |
| ------- | ----------- |
| `logs/`<br/>`*.notes`<br/>`pattern*/` | İstenilen desenleri içeren bir dosyayı, doğrudan dize eşleşmeleri veya joker karakter kümeleri ile .gitignore olarak kaydedin. |
| `git config --global core.excludesfile [dosya]` | Tüm yerel depolar için sistem genelinde örüntüyü yoksay |

### TEMPORARY COMMITS
_Dalları değiştirmek için değiştirilmiş, izlenen dosyaları geçici olarak depolayın_

| Komut | Açıklama |
| ------- | ----------- |
| `git stash` | Değiştirilen ve aşamalı değişiklikleri kaydet |
| `git stash list` | Saklanmış dosya değişikliklerinin yığın sırasını listele |
| `git stash pop` | Yığının tepesinden çalışarak yaz |
| `git stash drop` | Değişiklikleri stash yığınının üstünden atın |