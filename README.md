# Informatik-Logbog

#p5js

[Encrypt&Decrypt](https://editor.p5js.org/uffebruh/sketches/1GORA1_Oa)

[Aim trainer](https://editor.p5js.org/uffebruh/sketches/UieW3uZGf)

![GetImage](https://github.com/user-attachments/assets/0b24dae1-0e22-4b8e-a6d7-177af544a0e1)

[Serpinski triangle - ChatGPT](https://editor.p5js.org/uffebruh/sketches/mDqvnvzGW)

[Random number generator](https://editor.p5js.org/uffebruh/sketches/w0qUrMlWd)



# Klasselære


# Vejrstation project

Jeg stod for at skrive coden for optagelse af data og at sende den data vidre til et SD kort, den kode ligger her(skevet med ChatGPT)


  // Start SD card
  if (!SD.begin(CSPIN)) {
    Serial.println("SD card initialization failed!");
    while (1) {};  // Stop running
  }

  dht.begin();

  // Create/open file and write headers
  dataFile = SD.open("datalog.csv", FILE_WRITE);
  if (dataFile) {
    dataFile.println("Humidity (%),Temperature (C)");
    dataFile.close();
  } else {
    Serial.println("Error opening datalog.csv");
  }
}


  // Reading temperature or humidity takes about 250 milliseconds!
  // Sensor readings may also be up to 2 seconds 'old' (its a very slow sensor)
  h = dht.readHumidity();
  // Read temperature as Celsius
  t = dht.readTemperature();

  // Check if any reads failed and exit early (to try again).
  if (isnan(h) || isnan(t)) {
    lcd.print("Failed to read");
    lcd.setCursor(0, 1);
    lcd.print("from DHT sensor!");
    return;
  }


Jeg lavede en boks til vores komponenter, den var dog for lille så jeg endte med at redesigne den

![image](https://github.com/user-attachments/assets/d78db20c-eaae-47e9-932a-7620dab6130b)

Den orginale boks var 8x6x5 mens dene nye er 12x8x8. Der er huller til ledninger og skærm

![image](https://github.com/user-attachments/assets/d4e5a649-c0d8-491a-8324-acefdc9f45d4)
