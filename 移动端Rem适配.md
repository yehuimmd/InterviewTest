### �ƶ�������
- webҳ�������ֻ��ˣ�h5ҳ�棩
- ��ƽ̨
- ����webview����
- ����webkit

#### �������䷽��
- pc�˲���display��inline-block����div���Ӻ�����
- �ƶ�web�����ö��ߣ���Ȱٷֱȣ�**flex���Բ���**��meDIA QUERY **ý���ѯ**��

- **ý���ѯ**
  ���css��ͨ��ý�����ͣ�screen��print����ý�������max-width��
      
       @media screen and (max-width: 320px){
            /* css����Ļ���<=320pxʱ�����ʽ��Ч */
            .inner{
                float: left;
            }
        }
        @media screen and (min-width: 321px){
            .inner{
            }
        }

����ʵ����һ���򵥵ĺ��ź����ŵ���Ӧ

- **remԭ��**����
Rem����һ�����嵥λ��������px��
**����**�������HTML��Ԫ�ش�С������ͬʱҲ������Ϊ�߶ȺͿ�ȵĵ�λ��
**����ԭ��**����̬�޸�html��font-size���䣻rem��ͨ����ͬ��Ļ�Ĵ�С����html��Ԫ�ص�font-size�����Դ�С��ʵ�����䡣

        /* +_mediaʵ��*/
        @media screen and (max-width: 360px) and (min-width: 321px){
            html{
                font-size: 20px;
            }
        }
        @media screen and (max-width: 320px){
            html{
                font-size: 24px;
            }
        }

ͨ��JS��̬����font-size��

	//��ȡ�Ӵ����
    let htmlWidth = document.documentElement.clientWidth || document.body.clientWidth;
	        console.log(htmlWidth);
     let htmlDom = document.getElementsByTagName('html')[0];
	        htmlDom.style.fontSize = htmlWidth/10 + 'px';

##### rem����
- rem��׼ֵ����

    1rem = 16px
- rem��ֵ�����빹��

    170/16 = 170px
- rem��scss���ʹ�ã�node-sass��װ��
  Ҳ����ֱ�Ӱ�װsass����װ�̳�http://www.cnblogs.com/yehui-mmd/p/8035170.html��
- rem����ʵս
ͨ������������ӿ�����������

	let htmlDom = document.getElementsByTagName('html')[0];
	window.addEventListener('resize', (e)=>{
	    //��ȡ�Ӵ����
	    let htmlWidth = document.documentElement.clientWidth || document.body.clientWidth;
	    htmlDom.style.fontSize = htmlWidth/10 + 'px';
	})
	
����rem����ĺ�����ʹ�ã�sass�﷨��

	@function px2rem($px) {
	    $rem:37.5px;//iphone6
	    @return ($px / $rem) + rem;
	}
	.header{
	    width:100%;
	    height: px2rem(40px);
	    background-color: red;
	    padding-left: px2rem(23px);
	 }