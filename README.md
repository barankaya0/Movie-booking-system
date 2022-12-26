# Movie-booking-system
#include <stdio.h>
#include <stdlib.h>
void gecersiz(){
	printf("\nGecersiz deger girdiniz.\n\n");
}
void cizgi(){
	printf("------------------------------------------------------------------------------------------------\n");
}
int YasaGoreIndirimHesapla(){
	int yas=0;
	
	printf("Indirim icin yasinizi giriniz:");
	scanf("%d",&yas);
	if (yas>=1 && yas<=10){
		return 20;
	}
	else if(yas>=11 && yas<=17){
		return 10;
	}
	else return 5;
	

}

int main() {
	int q=0;
	int secim = 0;
	int film_id;
	char c1[20];
	char c2[20];
	int sayilar[]= {1,2,3,4,5,6,7,8,9,10,11,12};
	int matris[5][10] = {{1,2,3,4,5,6,7,8,9,10},{11,12,13,14,15,16,17,18,19,20},{21,22,23,24,25,26,27,28,29,30},{31,32,33,34,35,36,37,38,39,40},{40,41,42,43,44,45}};
	int w,e,n,b,s3,s4,bk,onay;
	float s1,s2,p;
	int f;
	int i = 38;
	int j = 42;
	int k = 39;
	int l = 44;
	while (secim !=5){
	
		//kullanıcıyı karşılayan ekran
		printf("Menu\n\n1:Filmlere Bak\n2:Bilet Satin Al\n3:Yeni Film Ekle\n4:Koltuk Duzenini Gor\n5:Cikis Yap\n\n");
	printf("Secim yapiniz:");
		scanf("%d",&secim);
		
	//seçimler ve içerikleri	
	switch(secim) {
		//filmler
		case 1:
			cizgi();
			printf("no.\t  Film adi\t\t    Turu\t\t Suresi\t\t Imdb puani\n");
			printf("1\tShutter Island\t\tGerilim/Gizem\t    2 saat 18 dakika\t   8.2/10\n");
			printf("2\tPulp Fiction\t\tSuc/Dram\t    2 saat 45 dakika\t   8.9/10\n");
			printf("3\tScarface\t\tSuc/Dram\t    2 saat 50 dakika\t   8.2/10\n");
			printf("4\tInterstellar\t\tBilim Kurgu/Macera  2 saat 49 dakika\t   8.6/10\n");
				if (onay==1){
			printf("%d\t%s\t\t\t%s\t    %d saat %d dakika\t   %.1f/10\n",n,c1,c2,s3,s4,p);
			cizgi();
			printf("\n");
			
				}
			else {
			cizgi();
			printf("\n");
			
			}
			
			
			break;
		//satın alma ekranı
		case 2:
			cizgi();
			printf("no.\t     Film adi\t\tBoyut\t   Baslangic/Bitis\t Bos Koltuk\t   Fiyat\n");
			printf("1\t  Shutter Island\t2D\t    14.00-16.18\t\t     %d\t\t   100 TL\n",i);
			printf("2\t  Pulp Fiction\t\t2D\t    16.00-18.45\t\t     %d\t\t   85 TL\n",j);
			printf("3\t  Scarface\t\t2D\t    18.00-20.50\t\t     %d\t\t   90 TL\n",k);
			printf("4\t  Interstellar\t\t3D\t    20.00-22.49\t\t     %d\t\t   100 TL\n",l);
				//yeni filmin eklendiği kısım
				if (onay==1){
			printf("%d\t  %s\t\t\t%dD\t    %.2f-%.2f\t\t     %d\t\t   %d TL\n",n,c1,b,s1,s2,bk,f);
			cizgi();
			printf("\n");
			
				}
			else {
			cizgi();
			printf("\n");
			}
			
			printf("\nFilm Seciniz: ");
			scanf("%d",&film_id);
			q=YasaGoreIndirimHesapla();
			printf("\n\n%d TL indirim kazandiniz.\n",q);
			
			if (film_id==1){
				i = i-1;
			printf("\nKalan Bos Koltuk Sayisi: %d\n\n\n",i);
			}
			else if (film_id==2){
				j = j-1;
			printf("\nKalan Bos Koltuk Sayisi: %d\n\n\n",j);
			}
			else if (film_id==3){
				k = k-1;
			printf("\nKalan Bos Koltuk Sayisi: %d\n\n\n",k);
			}
			else if (film_id==4){
				l = l-1;
			printf("\nKalan Bos Koltuk Sayisi: %d\n\n\n",l);
			}
			else if (film_id==5){
				bk = bk-1;
			printf("\nKalan Bos Koltuk Sayisi: %d\n\n\n",bk);
			}
			else{
				gecersiz();
			}
			break;
		//film ekleme kısmı	
		case 3:
		
			printf("%d-Film no. giriniz:\n",sayilar[0]);
			scanf("%d",&n);
			printf("%d-Film ismi giriniz:\n",sayilar[1]);
			scanf("%s",&c1);
			printf("%d-Film turu giriniz:\n",sayilar[2]);
			scanf("%s",&c2);
			printf("%d-Film boyutu giriniz:\n",sayilar[3]);
			scanf("%d",&b);
			printf("%d-Film baslangic saatini giriniz:\n",sayilar[4]);
			scanf("%f",&s1);
			printf("%d-Film bitis saatini giriniz:\n",sayilar[5]);
			scanf("%f",&s2);
			printf("%d-Film suresinin saat kismini giriniz:\n",sayilar[6]);
			scanf("%d",&s3);
			printf("%d-Film suresinin dakika kismini giriniz:\n",sayilar[7]);
			scanf("%d",&s4);
			printf("%d-Film imdb puanini giriniz:\n",sayilar[8]);
			scanf("%f",&p);
			printf("%d-Film bilet fiyatini giriniz:\n",sayilar[9]);
			scanf("%d",&f);
			printf("%d-Salonun koltuk sayisini giriniz:\n",sayilar[10]);
			scanf("%d",&bk);
			printf("%d-Film eklemeyi onayliyorsaniz 1'e basiniz:\n",sayilar[11]);
			scanf("%d",&onay);
			
			break;
		//matris		
		case 4:
			for (w=0 ; w<5 ;w++){
			
			
				for (e=0; e<10;e++){
					printf("%d--- ",matris[w][e]);
					
				}
			printf("\n\n\n\n\n");
			
			}
			break;
		//döngüyü sonlandırmak için
		case 5:
			printf("\n\nUygulamayi Kapatmak Icin Herhangi Bir Tusa Basiniz.\n");
			
			break;
		
		default:
			gecersiz();
			break;
		
		
		}
			
	
	}

	
	return 0;
}
