# �ۑ�2 ���|�[�g


�W���摜�uice�v�����摜�Ƃ���.���̉摜�͏c480��f,��640��f�̒����`�̃f�B�W�^���J���[�摜�ł���.  

ORG=imread('ice.jpg'); % ���摜�̓���  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % �摜�̕\��  

�ɂ����,���m�N���ɏ���,�\���������ʂ�}1�Ɏ���.  
![���m�N���摜](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai02/kadai02_0gen.jpg?raw=true)  
�}1 ���m�N���摜  

�摜���~���ŕ�����ɂ�,�摜�̐F�f�[�^�ɑ΂���臒l��������,����ɂ�菈���������Ă��΂悢.  
����2�~���ŕ\������������,�摜�ɑ΂�128�Ƃ���臒l��^���ď������Ă���.  

IMG = ORG>128;  
imagesc(IMG); colormap(gray); colorbar; axis image;  

�\�����ꂽ���ʂ�}2�Ƃ��Ď���.  
![2�K���摜](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai02/kadai02_2dan.jpg?raw=true)  
�}2 2�K���摜  

���l���~���𑝂₵�����Ȃ��,臒l�𕡐��^���Ă��΂悢.  
����4�~���ŕ\������������,���l��  

IMG0 = ORG>64;  
IMG1 = ORG>128;  
IMG2 = ORG>192;  
IMG = IMG0 + IMG1 + IMG2;  
imagesc(IMG); colormap(gray); colorbar; axis image;  

��臒l�𑝂₷.�\�����ꂽ���ʂ�}3�Ƃ��Ď���.  
![4�K���摜](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai02/kadai02_4dan.jpg?raw=true)  
�}3 4�K���摜  

���K���ł����l�ł���,���������~����臒l�𑝂₵�Ă��΂悢.  

IMG0=ORG>32;  
IMG1=ORG>64;  
IMG2=ORG>96;  
IMG3=ORG>128;  
IMG4=ORG>160;  
IMG5=ORG>192;  
IMG6=ORG>224;  
IMG=IMG0+IMG1+IMG2+IMG3+IMG4+IMG5+IMG6;  
imagesc(IMG); colormap(gray); colorbar; axis image;  

�\�����ꂽ���ʂ�}3�Ƃ��Ď���.  
![4�K���摜](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai02/kadai02_8dan.jpg?raw=true)  
�}4 8�K���摜  

���̂悤��,�~����������ƐF�ʂ������邱�Ƃ��킩��.