# ‰Û‘è1 ƒŒƒ|[ƒg

•W€‰æ‘œuicev‚ğŒ´‰æ‘œ‚Æ‚·‚é.‚±‚Ì‰æ‘œ‚Íc480‰æ‘f,‰¡640‰æ‘f‚Ì’·•ûŒ`‚ÌƒfƒBƒWƒ^ƒ‹ƒJƒ‰[‰æ‘œ‚Å‚ ‚é.  

ORG=imread('Lenna.png'); % Œ´‰æ‘œ‚Ì“ü—Í  
ORG= rgb2gray(ORG); % ƒJƒ‰[‰æ‘œ‚ğ”’•”Z’W‰æ‘œ‚Ö•ÏŠ·  
imagesc(ORG); colormap(gray); colorbar; % ‰æ‘œ‚Ì•\¦  

‚É‚æ‚Á‚Ä,Œ´‰æ‘œ‚ğ“Ç‚İ‚İ,ƒJƒ‰[‰æ‘œ‚ğ”’•”Z’W‰æ‘œ‚Ö•ÏŠ·,•\¦‚µ‚½Œ‹‰Ê‚ğ}1‚É¦‚·.  
![”’•”Z’W‰æ‘œ](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai03/kadai3_0_noutan.jpg?waw=true)  
}1 ”’•”Z’W‰æ‘œ  


Ÿ‚Í‹P“x’l‚É‚æ‚Á‚Ä‰æ‘f‚Éˆ—‚ğ•Ï‚¦‚é.  
‚Í‚¶‚ß‚É,‹P“x’l‚ª64ˆÈã‚Ì‰æ‘f‚ğ1C‚»‚Ì‘¼‚ğ0‚É•ÏŠ·‚Æ‚µ‚½ˆ—‚ğ—^‚¦‚é.  

IMG = ORG > 64; % ‹P“x’l‚ª64ˆÈã‚Ì‰æ‘f‚ğ1C‚»‚Ì‘¼‚ğ0‚É•ÏŠ·
imagesc(IMG); colormap(gray); colorbar;  

‚»‚ÌŒ‹‰Ê‚ğ}2‚É¦‚·.  
![”’•”Z’W‰æ‘œ 64](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai03/kadai3_64.jpg?waw=true)  
}2 ”’•”Z’W‰æ‘œ 64  


Ÿ‚É,‹P“x’l‚ª96ˆÈã‚Ì‰æ‘f‚ğ1C‚»‚Ì‘¼‚ğ0‚É•ÏŠ·‚Æ‚µ‚½ˆ—‚ğ—^‚¦‚é.  

IMG = ORG > 96;  
imagesc(IMG); colormap(gray); colorbar;  

‚»‚ÌŒ‹‰Ê‚ğ}3‚É¦‚·.  
![”’•”Z’W‰æ‘œ 96](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai03/kadai3_96.jpg?waw=true)  
}3 ”’•”Z’W‰æ‘œ 96  

Ÿ‚É,‹P“x’l‚ª128ˆÈã‚Ì‰æ‘f‚ğ1C‚»‚Ì‘¼‚ğ0‚É•ÏŠ·‚Æ‚µ‚½ˆ—‚ğ—^‚¦‚é.  

IMG = ORG > 128;  
imagesc(IMG); colormap(gray); colorbar;  

‚»‚ÌŒ‹‰Ê‚ğ}4‚É¦‚·.  
![”’•”Z’W‰æ‘œ 128](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai03/kadai3_128.jpg?waw=true)  
}4 ”’•”Z’W‰æ‘œ 128  

ÅŒã‚É,‹P“x’l‚ª192ˆÈã‚Ì‰æ‘f‚ğ1C‚»‚Ì‘¼‚ğ0‚É•ÏŠ·‚Æ‚µ‚½ˆ—‚ğ—^‚¦‚é.  

IMG = ORG > 192;  
imagesc(IMG); colormap(gray); colorbar;  

‚»‚ÌŒ‹‰Ê‚ğ}5‚É¦‚·.  
![”’•”Z’W‰æ‘œ 192](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai03/kadai3_192.jpg?waw=true)  
}5 ”’•”Z’W‰æ‘œ 192  

‹P“x’l‚Ìè‡’l‚ğ‚‚­‚·‚é‚±‚Æ‚É‚æ‚Á‚Ä,ğŒ‚É‚©‚©‚é”’l‚ª‘½‚­‚È‚è,Œ‹‰Ê‚Æ‚µ‚Ä‰æ‘œ‚ª•‚­‚È‚é‰æ‘f‚ª‘½‚­‚È‚é‚±‚Æ‚ª‚í‚©‚é.  