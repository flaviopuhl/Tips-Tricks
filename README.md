# Tips-Tricks

Serial Monitor
  // All information in only one line
  // Nem line as ASCII caracter
  // String saved on flash to save RAM
  
  float x;
  float y;
  String PROGMEM local = (String)"data_non-filtered: "+ x + " data_filtered: " + y +"\n";
    Serial.print(local);
    


Serial Plot
  // In order to plot multiple variables or waveforms simultaneously a 'space' is printed between the two print statements.

  Serial.print(x);
  Serial.print(" ");
  Serial.println(y);



First Order Filter
 
   float data = digitalRead(2);
    data_filtered[n] = alpha * data + (1 - alpha) * data_filtered[n-1];
    data_filtered[n-1] = data_filtered[n];
  	
