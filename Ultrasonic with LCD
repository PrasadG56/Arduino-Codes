#include<LiquidCrystal.h>
const int contrast = 97, rst = 10, en = 9, d7 = 2, d6 = 3, d5 = 4, d4 = 5;
#define echo 7
#define trig 6
LiquidCrystal lcd(rst, en, d4, d5, d6, d7);
void setup() {
  pinMode(echo, INPUT);
  pinMode(trig, OUTPUT);
  lcd.begin(16, 2);
  analogWrite(11, contrast);
  lcd.clear();
}

void loop() {
  digitalWrite(trig, LOW);
  delayMicroseconds(2);
  digitalWrite(trig, HIGH);
  delayMicroseconds(10);
  int durat = pulseIn(echo, HIGH);
  float dist = (durat * 0.034)/2;
  lcd.setCursor(0, 0);
  lcd.print("distance: ");
  delay(500);
  lcd.setCursor(0, 1);
  lcd.print(dist);
}
