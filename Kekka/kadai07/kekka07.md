# �ۑ�7 ���|�[�g 

��f�̃_�C�i�~�b�N�����W��0����255�Ƃ���.   
�W���摜�uice�v�����摜�Ƃ���.���̉摜�͏c480��f,��640��f�̒����`�̃f�B�W�^���J���[�摜�ł���.  

ORG=imread('Lenna.png'); % ���摜�̓���  
ORG=rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  
imagesc(ORG); colormap(gray); colorbar;  

�ɂ����,�����Z�W�摜�ɕύX���ꂽ���ʂ�}1�Ɏ���.  
![�����Z�W�摜](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai07/kadai07_00.jpg?raw=true)  
�}1 �����Z�W�摜  

����,�Z�x�q�X�g�O�������o�͂���.  

imhist(ORG); % �Z�x�q�X�g�O�����𐶐��A�\��  

�ɂ���ďo�͂��ꂽ���ʂ�}3�Ɏ���.  
![�Z�x�q�X�g�O����](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai07/kadai07_01.jpg?raw=true)  
�}2 �Z�x�q�X�g�O����  

����,�摜�̃_�C�i�~�b�N�����W��0�`255�ƒ��,�������s��.  

ORG = double(ORG);  
mn = min(ORG(:)); % �Z�x�l�̍ŏ��l���Z�o  
mx = max(ORG(:)); % �Z�x�l�̍ő�l���Z�o  
ORG = (ORG-mn)/(mx-mn)*255;  
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��  

���̌��ʂ�}3�Ɏ���.  
![�_�C�i�~�b�N�����W0�`255](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai07/kadai07_02.jpg?raw=true)  
�}3 �_�C�i�~�b�N�����W0�`255

�Ō��,���̔Z�x�q�X�g�O�������o�͂���.

ORG = uint8(ORG); % ���̍s�ɂ��čl�@����  
imhist(ORG); % �Z�x�q�X�g�O�����𐶐��A�\��  

���̌��ʂ�}4�Ɏ���.  
![�_�C�i�~�b�N�����W0�`255�Z�x�q�X�g�O����](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai07/kadai07_03.jpg?raw=true)  
�}4 �_�C�i�~�b�N�����W0�`255�Z�x�q�X�g�O����

ORG = uint8(ORG)�ɂ���  
���ނ̃q�X�g�O�������r�����uint8���s�����O�����ł͏c�̃O���t10�{���Ƃɋ󔒂��}������Ă��邱�Ƃ��킩��.  


�摜�ł͂킩��Â炢��,�_�C�i�~�b�N�����W�̏������s������ł͉E�̃O���t����0�̐��l�������Ă���,�摜�̃f�[�^�T�C�Y��29.8k�o�C�g����29.1k�o�C�g�ւƏ������Ȃ���.  
�����ĉ摜�̕��������Z���Ȃ��Ă���.  