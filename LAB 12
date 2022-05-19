; RM-Shao 2022.5.5
; R3 is a cursor to indicate where is the target number, R2 is to hold temp variable, R5 is to hold sum, R4 is a counter

0011 0001 0000 0000; x3100 - starting address of the program

;initialize variable
1110 011 000110001 ; LEA R3 x31 initialize R3<-x3132
0101 100 100 100000; AND R4, R4, #0, initialize R4 <-0
0001 100 100 101010; ADD R4, R4, #10, initialize R4<-10
0101 101 101 100000; AND R5, R5, #0, initialize R5 <-0

; main loop
0110 010 011 000000 ; LDR R2 R3 #0, load the pointed number
0000 110 000000001  ; BRnz #1, if num is negative, ignore and do R3+1 R4-1
0001 101 101 000 010; ADD R5 R5 R2, get sum
0001 011 011 1 00001; R3<-R3+1
0001 100 100 1 11111; R4<-R4-1
0000 001 111111010  ; BRn #-6, if R4>0,loop
; end loop

1111 0000 0010 0101 ; halt
