# �ۑ�1 ���|�[�g

�W���摜�uice�v�����摜�Ƃ���.���̉摜�͏c480��f,��640��f�̒����`�̃f�B�W�^���J���[�摜�ł���.  

ORG=imread('Lenna.png'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��  

�ɂ����,���摜��ǂݍ���,�J���[�摜�𔒍��Z�W�摜�֕ϊ�,�\���������ʂ�}1�Ɏ���.  
![�����Z�W�摜](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai03/kadai3_0_noutan.jpg?waw=true)  
�}1 �����Z�W�摜  


���͋P�x�l�ɂ���ĉ�f�ɏ�����ς���.  
�͂��߂�,�P�x�l��64�ȏ�̉�f��1�C���̑���0�ɕϊ��Ƃ���������^����.  

IMG = ORG > 64; % �P�x�l��64�ȏ�̉�f��1�C���̑���0�ɕϊ�
imagesc(IMG); colormap(gray); colorbar;  

���̌��ʂ�}2�Ɏ���.  
![�����Z�W�摜 64](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai03/kadai3_64.jpg?waw=true)  
�}2 �����Z�W�摜 64  


����,�P�x�l��96�ȏ�̉�f��1�C���̑���0�ɕϊ��Ƃ���������^����.  

IMG = ORG > 96;  
imagesc(IMG); colormap(gray); colorbar;  

���̌��ʂ�}3�Ɏ���.  
![�����Z�W�摜 96](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai03/kadai3_96.jpg?waw=true)  
�}3 �����Z�W�摜 96  

����,�P�x�l��128�ȏ�̉�f��1�C���̑���0�ɕϊ��Ƃ���������^����.  

IMG = ORG > 128;  
imagesc(IMG); colormap(gray); colorbar;  

���̌��ʂ�}4�Ɏ���.  
![�����Z�W�摜 128](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai03/kadai3_128.jpg?waw=true)  
�}4 �����Z�W�摜 128  

�Ō��,�P�x�l��192�ȏ�̉�f��1�C���̑���0�ɕϊ��Ƃ���������^����.  

IMG = ORG > 192;  
imagesc(IMG); colormap(gray); colorbar;  

���̌��ʂ�}5�Ɏ���.  
![�����Z�W�摜 192](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai03/kadai3_192.jpg?waw=true)  
�}5 �����Z�W�摜 192  

�P�x�l��臒l���������邱�Ƃɂ����,�����ɂ����鐔�l�������Ȃ�,���ʂƂ��ĉ摜�������Ȃ��f�������Ȃ邱�Ƃ��킩��.  