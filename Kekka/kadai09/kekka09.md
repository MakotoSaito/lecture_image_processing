# �ۑ�9 ���|�[�g 

���f�B�A���t�B���^�[��K�p���C�m�C�Y�������s��.  
�W���摜�uice�v�����摜�Ƃ���.���̉摜�͏c480��f,��640��f�̒����`�̃f�B�W�^���J���[�摜�ł���.  

�܂��͌��摜�𔒍��Z�W�摜�ɕϊ�����.  

ORG=imread('Lenna.png'); % ���摜�̓���  
ORG=rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  
imagesc(ORG); colormap(gray); colorbar;  

�ɂ����,�����Z�W�摜�ɕύX���ꂽ���ʂ�}1�Ɏ���.  
![�����Z�W�摜](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai09/kadai09_00.jpg?raw=true)  
�}1 �����Z�W�摜  

����,�m�C�Y�̏������s���O�Ƀm�C�Y�̍ڂ����摜���쐬����.  

ORG = imnoise(ORG,'salt & pepper',0.02); % �m�C�Y�Y�t  
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��  

���̌��ʂ�}2�Ɏ���.  
![�m�C�Y�Y�t](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai09/kadai09_01.jpg?raw=true)  
�}2 �m�C�Y�Y�t  

����,�������t�B���^�ł̃m�C�Y�̏������s��.  

IMG = filter2(fspecial('average',3),ORG); % �������t�B���^�ŎG������  
imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��  

���̌��ʂ�}3�Ɏ���.  
![�������t�B���^](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai09/kadai09_02.jpg?raw=true)  
�}3 �������t�B���^  

����,���f�B�A���t�B���^�ł̃m�C�Y�̏������s��.  

IMG = medfilt2(ORG,[3 3]); % ���f�B�A���t�B���^�ŎG������  
imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��  

���̌��ʂ�}4�Ɏ���.  
![���f�B�A���t�B���^](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai09/kadai09_03.jpg?raw=true)  
�}4 ���f�B�A���t�B���^  

�Ō��,����t�B���^��݌v��,�K�p,�������s��.  

f=[0,-1,0;-1,5,-1;0,-1,0]; % �t�B���^�̐݌v  
IMG = filter2(f,IMG,'same'); % �t�B���^�̓K�p  
imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��  

���̌��ʂ�}5�Ɏ���.  
![�t�B���^�̐݌v,�K�p](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai09/kadai09_04.jpg?raw=true)  
�}5 �t�B���^�̐݌v,�K�p  


