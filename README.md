# Raka
Kode Program jam Digital simulasi keil Proteus menggunakan mikroprosesor AT89C51
//jam Digital simulasi keil Proteus
#include<reg51.h>

void main()
{
	int t,i,j,k,a,b,c,d,e;
	e=0;
	P3=0x00;
	P2=0x00;
	P0=0x00;
	while(1)
	{ P0=0x00;
		for(c=0;c<3;c++)
		{
			for(d=0;d<10;d++)
			{
				for(a=0;a<6;a++)
				{
					for(b=0;b<10;b++)
					{
						for(t=0;t<6;t++)
						{
							for(i=0;i<10;i++)
							{
								for(k=0;k<1000;k++)
								for(j=0;j<142;j++);
								P3++;
							}
							P3=P3+0x06;
						}
						P3=0x00;
						P2++;
					}
					P2=P2+0x06;
				}
				P2=0x00;
				P0++;
				if(P0==0x24)
				{
					P0=0x00;
					e=1;}
				if(e==1)
					break;
			}
			P0=P0+0x06;
		}
	}
}						
