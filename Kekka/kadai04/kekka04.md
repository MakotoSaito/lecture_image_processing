# �ۑ�4 ���|�[�g

�W���摜�uice�v�����摜�Ƃ���.���̉摜�͏c480��f,��640��f�̒����`�̃f�B�W�^���J���[�摜�ł���.  
���摜����������,��f�̔Z�x�q�X�g�O�������쐬����.  

ORG=imread('Lenna.png'); % ���摜�̓���  
ORG=rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  
imagesc(ORG); colormap(gray); colorbar;  

�ɂ����,�����Z�W�摜�ɕύX���ꂽ���ʂ�}1�Ɏ���.  
�ɂ����,�����Z�W�摜�ɕύX���ꂽ�摜�̃q�X�g�O�����̌��ʂ�}1�Ɏ���.  
![�����Z�W�摜](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai04/kadai04_noutan.jpg?waw=true)  
�}1 �����Z�W�摜  

���̌�,���̉摜�̃q�X�g�O������\������.

imhist(ORG); % �q�X�g�O�����̕\��  

���̌��ʂ�}2�Ɏ���.  

![�����Z�W�摜�q�X�g�O����](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai04/kadai04_noutan_hist.jpg?waw=true)  
�}1 �����Z�W�摜�q�X�g�O����  

���摜�𔒍��Z�W�摜�ɕύX������,�q�X�g�O�����Ƃ��ďo�͂��ꂽ���Ƃ��킩��.  
