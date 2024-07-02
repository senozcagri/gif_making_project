#öncelikle terminal kısmına parantez içindeki kodu (pip3 install imageio) yazıp gerekli dosyaları indiriyoruz.

#ardından import komutuyla çağırıyoruz.
#Import ifadesindeki "v3", imageio kitaplığının 3. sürümünü kullandığınız anlamına gelir.

import imageio.v3 as iio

#Not: indirdiğiniz image dosyalarını Python program dosyanızla aynı klasörde sakladığınızdan emin olun.

filenames = ['team-pic1.png', 'team-pic2.png']
images = [ ]
for filename in filenames:
  images.append(iio.imread(filename))
  iio.imwrite('team.gif', images, duration=500, loop=0)


#Bu dört argüman gerektirir:
#'team.gif': Yeni GIF dosyanıza vermek istediğiniz addır.
#images: Resim verilerini içeren liste.
#duration = süre, 500: Her bir resmin GIF'te milisaniye cinsinden ne kadar süreyle gösterilmesi gerektiği.
#loop = döngü = 0: GIF'in kaç kez tekrarlanması gerektiği (0, sonsuza kadar döngüye devam edeceği anlamına gelir).
  
