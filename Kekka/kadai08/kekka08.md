# �ۑ�8 ���|�[�g 

��l�����ꂽ�摜�̘A�������Ƀ��x�����s��.  
�W���摜�uice�v�����摜�Ƃ���.���̉摜�͏c480��f,��640��f�̒����`�̃f�B�W�^���J���[�摜�ł���.  

ORG=imread('Lenna.png'); % ���摜�̓���  
ORG=rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  
imagesc(ORG); colormap(gray); colorbar;  

�ɂ����,�����Z�W�摜�ɕύX���ꂽ���ʂ�}1�Ɏ���.  
![�����Z�W�摜](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai08/kadai08_00.jpg?raw=true)  
�}1 �����Z�W�摜  


����,臒l128�ŉ摜�̓�l�����s��. 

IMG = ORG > 128; % 臒l128�œ�l��  
imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��  

���̌��ʂ�}2�Ɏ���.  
![��l��](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai08/kadai08_01.jpg?raw=true)  
�}2 ��l��  

�Ō��,�o�C�i�� �C���[�W���̘A���v�f�����x���t�����s��.  

IMG = bwlabeln(IMG); 
imagesc(IMG); colormap(jet); colorbar; % �摜�̕\��  
���̌��ʂ�}3�Ɏ���.  
![�A���v�f�̃��x���t��](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai08/kadai08_03.jpg?raw=true)  
�}3 �A���v�f�̃��x���t��  

�o�͌��ʂ��,�����F�ʂ����ꏊ�������F�ŕ\������Ă��邱�Ƃ��킩��.  