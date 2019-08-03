Analog I/O
=====

Maixduino uses the pwm module of the K210 chip to implement the analogWrite() function. The analogRead() function is temporarily unavailable.

In Maixduino, you can configure up to 12 pins of the 48 FPIOs to be Analog Output.

----
## analogWrite()

### Description
Writes an analog value (PWM wave) to a pin. Can be used to light a LED at varying brightnesses or drive a motor at various speeds. 

### Syntax

`analogWrite(pin, value)`

### Parameters
`pin`: the pin to write to. Allowed data types: `int`.
`value`: the duty cycle: between 0 (always off) and 255 (always on). Allowed data types: `int`

### Returns
Nothing

### Notes and Warnings

The timer and PWM functions may have an interaction.

----
## analogWriteResolution()

### Description
`analogWriteResolution()` is an extension of the Analog API for the Maixduino.

`analogWriteResolution()` sets the resolution of the `analogWrite()` function. It defaults to 8 bits (values between 0-255) for compatibility with AVR based boards.


By setting the write resolution to 12, you can use `analogWrite()` with values between 0 and 4095 to set the PWM signal without rolling over.

### Syntax

`analogWriteResolution(bits)`

### Parameters
`bits`: determines the resolution (in bits) of the values used in the analogWrite() function. The value can range from 1 to 32. 

### Returns
Nothing

### Notes and Warnings

Passing the PWM duty cycle may not result in significant accuracy variations.

### Example Code
```
int led1 = 12;
int led2 = 13;
int led3 = 14;

void setup()
{
  pinMode(led1,OUTPUT);
  pinMode(led2,OUTPUT);
  pinMode(led3,OUTPUT);
}
void setColor(int red,int green,int blue)
{
  analogWrite(led1,255-red);
  analogWrite(led2,255-green);
  analogWrite(led3,255-blue);
}
void loop()
{
  int i,j;
  for(i=0,j=255;i<256;i++)
  {
    setColor(i,j,0);
    delay(4);
    j--;
  }
  delay(100);           
  for(i=0,j=255;i<256;i++)
  {
    setColor(j,0,i);
    delay(4);
    j--;
  }
  delay(100);           
  for(i=0,j=255;i<256;i++)
  {
    setColor(0,i,j);
    delay(4);
    j--;
  }
  delay(100);        
}
```
