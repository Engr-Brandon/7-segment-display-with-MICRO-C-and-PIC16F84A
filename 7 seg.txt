/*
    Counter from 0 to 9 using a 7 segment display
    */

void main(){
    TRISB=0x00;  // All PORT B as output
    while(1){
    int i=0;
       unsigned char count[10]={0x3F,0x06,0x5B,0x4F,0x66,0x6D,0x7D,0x07,0xFF,0x6F};
        while(i<10){
            PORTB=count[i];
            delay_ms(200);
            i++;
        }
    }
}