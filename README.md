# SERIAL-TRANSFER-OF-SINGLE-BYTE-CHARACTER-USING-8051-KEIL.-EMBEDDED-C-PROGRAM-

**AIM:** 

To write and execute Embedded C Program for Serial Transfer of Single Byte / Character using 8051 KEIL

**APPARATUS REQUIRED:**

Personal computer with Keil software

**PROGRAM:**

**(i)	Serial port transfer a character A**

#include<reg51.h> void main(void)

{

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

while(1)

{ SBUF='A';

while(TI==0); TI=0;

}

}

**(ii)	Serial port to Transfer a Message**

#include<reg51.h> void main(void)

{

unsigned char msg[]="MESSAGE"; unsigned char i;

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

for (i=0; i<17;i++)

{

SBUF= msg[i]; while(TI==0); TI=0;

}

while(1);

}

 
**OUTPUT:**
<img width="943" height="204" alt="Screenshot 2025-10-27 105616" src="https://github.com/user-attachments/assets/e1bbc85b-c394-4ad9-8549-19dc511052bd" />
<img width="180" height="65" alt="Screenshot 2025-10-27 105123" src="https://github.com/user-attachments/assets/901033a2-a25f-44e6-a112-93fdc783df50" />


**Result:**

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
