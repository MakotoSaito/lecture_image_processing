# �ۑ�6 ���|�[�g 

�W���摜�uice�v�����摜�Ƃ���.���̉摜�͏c480��f,��640��f�̒����`�̃f�B�W�^���J���[�摜�ł���.  
�摜��

ORG=imread('Lenna.png'); % ���摜�̓���  
ORG=rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  
imagesc(ORG); colormap(gray); colorbar;  

�ɂ����,�����Z�W�摜�ɕύX���ꂽ���ʂ�}1�Ɏ���.  
![�����Z�W�摜](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai06/kadai06_00.jpg?raw=true)  
�}1 �����Z�W�摜  


����,臒l��128�Ƃ��Ă̓�l�����s��. 

IMG = ORG>128; % 128�ɂ���l��  
imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��  
pause;  

�ɂ����,��l�����ꂽ���ʂ�}2�Ɏ���.  
![臒l�ɂ���l��](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai06/kadai06_01.jpg?raw=true)  
�}2 臒l�ɂ���l��  

�Ō��,�f�B�U�@�ɂ���l�����s��.  

IMG = dither(ORG); % �f�B�U�@�ɂ���l��  
imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��  

�ɂ����,��l�����ꂽ���ʂ�}3�Ɏ���.  
![�f�B�U�@�ɂ���l��](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai06/kadai06_02.jpg?raw=true)  
�}3 �f�B�U�@�ɂ���l��  

�o�͌��ʂ��,臒l�ɂ���l���ł͂��ꂢ�ɏo�͂ł��Ă���̂ɑ΂�,�f�B�U�@�ł͐���̃m�C�Y�̂悤�Ȃ��̂������Ă��邱�Ƃ��킩��.  
