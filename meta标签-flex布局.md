#### meta ��ǩ
- name='viewport'//ʵ��һЩ�ƶ�������Ĳ���

#### flex���Բ���

    flex: 1
    
�����е��Ժ�ģ�Ͷ������Ԫ�ض�����ͬ�ĳ��ȣ��Һ��������ڲ������ݡ�

##### flex����
�κ�����������flex���֡�Flex������������Ԫ��Ҳ�Զ���Ϊ�����ĳ�Ա����ΪFlex��Ŀ��Flex����Ĭ�ϴ���2�����ߣ�ˮƽ����ʹ�ֱ�����ᣩ,���־��Ǹ�����2������������Ŀ��ʾ�ġ�

	�鼶Ԫ�أ�display:flex;
	����Ԫ�أ�display:inlne-flex;

 ʹ����flex���ֺ���Ŀ��**float��clear��vertical-align**����ʧȥЧ����

##### Flex��������
- flex-direction��������Ŀ�����з���

    flex-direction: row | row-reverse | column | column-reverse;

- flex-wrap��������Ŀ�Ƿ�������

    flex-wrap: nowrap | wrap | wrap-reverse; 
 
 - flex-flow��flex-direction���Ժ�flex-wrap���Եļ�д��ʽ��Ĭ��ֵΪrow nowrap
 
     flex-flow: <flex-direction> || <flex-wrap>;
 
 - justify-content��������Ŀ��ˮƽ���뷽ʽ
 
     justify-content: flex-start | flex-end | center | space-between | space-around;
 
  flex-start��Ĭ��ֵ���������
  flex-end���Ҷ���
  center�� ����
  space-between�����˶��룬��Ŀ֮��ļ������ȡ�
  space-around��ÿ����Ŀ����ļ����ȡ����ԣ���Ŀ   ֮��ļ������Ŀ��߿�ļ����һ����

- align-items��������Ŀ��ֱ������뷽ʽ��
   
     align-items: flex-start | flex-end | center | baseline | stretch;
flex-start��������������롣
flex-end����������յ���롣
center����������е���롣
baseline: ��Ŀ�ĵ�һ�����ֵĻ��߶��롣
stretch��Ĭ��ֵ���������Ŀδ���ø߶Ȼ���Ϊauto����ռ�����������ĸ߶ȡ�

##### 
#### css hack
- ����

  css hack ��ͨ����css ��ʽ�м���һЩ����ķ��ţ��ò�ͬ�������ʶ��ͬ�ķ��ţ��ѵ��ﲻͬ��css��ʽ��Ŀ�ġ�����**.kwstu{width:300px;_width:200px;}**��һ����������ȸ�Ԫ��ʹ��width:300px;����ʽ�������ź��滹�и�**_width:200px;�����»���_widthֻ��IE6����ʶ�����Դ���ʽ��IE6��ʵ�����ö���Ŀ��Ϊ200px��**����İ�ǰ��ĸ������ˣ��������������ʶ��_width����ִ��_width:200px��**����ʹ��css hack������ּ���������**��
  
- Ϊʲô���Ƽ�ʹ��CSS hack�������������

 CSS hack����Ϊ����������Ա�׼�Ľ�����ͬ��Ϊ�˼��ݸ�������������õ�һ�ֲ��ȷ�����CSS hack��һ������**����**���ֶΣ�����ƭ������ķ�ʽ�ﵽ���ݵ�Ŀ�ģ�����������ļ����Բ��������������ļ��������⡣��ˣ������֮����дCSS hack��Ҫ��ѭ��������ԭ��
1. ��Ч�� �ܹ�ͨ�� Web ��׼����֤
2. ֻ���̫���ϵ�/���ٿ�����/�ѱ�������������� ������Ŀǰ�����������
3. ����Ҫ��ª�����˼�ס����һ�������Ѷ�Ϊ֮�� Hack, ʱ�̼�סҪ��취ȥ���������ںܶ�hacks�Ѿ������������ԭ�򣬶�����hack�ᵼ�����������֮���������ļ��������⡣