# �ۑ�10 ���|�[�g 

�摜�̃G�b�W���o���s��.  
�W���摜�uice�v�����摜�Ƃ���.���̉摜�͏c480��f,��640��f�̒����`�̃f�B�W�^���J���[�摜�ł���.  

ORG=imread('ice.jpg'); % ���摜�̓���  
ORG=rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  
imagesc(ORG); colormap(gray); colorbar;  

�ɂ����,�����Z�W�摜�ɕύX���ꂽ���ʂ�}1�Ɏ���.  
![�����Z�W�摜](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai10/kadai10_00.jpg?raw=true)  
�}1 �����Z�W�摜  

����,�v���E�B�b�g�@�ł̃G�b�W���o���s��.  

IMG = edge(ORG,'prewitt'); % �G�b�W���o�i�v���E�B�b�g�@�j  
imagesc(IMG); colormap('gray'); colorbar;% �摜�\��  

���̌��ʂ�}2�Ɏ���.  
![�G�b�W���o�i�v���E�B�b�g�@�j](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai10/kadai10_01.jpg?raw=true)  
�}2 �G�b�W���o�i�v���E�B�b�g�@�j  

����,�\�x���@�ł̃G�b�W���o���s��.  

IMG = edge(ORG,'sobel'); % �G�b�W���o�i�\�x���@�j  
imagesc(IMG); colormap('gray'); colorbar;% �摜�\��  

���̌��ʂ�}3�Ɏ���.  
![�G�b�W���o�i�\�x���@�j](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai10/kadai10_02.jpg?raw=true)  
�}3 �G�b�W���o�i�\�x���@�j  

�Ō�ɃL���j�[�@�ł̃G�b�W���o���s��.  

IMG = edge(ORG,'canny'); % �G�b�W���o�i�L���j�[�@�j  
imagesc(IMG); colormap('gray'); colorbar;% �摜�\��  

���̌��ʂ�}4�Ɏ���.  
![�G�b�W���o�i�L���j�[�@�j](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai10/kadai10_03.jpg?raw=true)  
�}4 �G�b�W���o�i�L���j�[�@�j  