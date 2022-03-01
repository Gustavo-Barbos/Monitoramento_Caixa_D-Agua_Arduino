# Monitoramento_Caixa_D-Agua_Arduino
Monitoramento do nível da água na caixa d'agua com arduino. 

## Código

// C++ code

int valor_carga1 = 0;
int valor_carga2 = 0;
int valor_carga3 = 0;
int valor_carga4 = 0;
int valor_carga5 = 0;
int valor_carga6 = 0;

void setup(){ 
   int j=0;
  
    pinMode(A0, INPUT);
    Serial.begin(9600);
    pinMode(A1, INPUT);
    Serial.begin(9600);
    pinMode(A2, INPUT);
    Serial.begin(9600);
    pinMode(A3, INPUT);
    Serial.begin(9600);
    pinMode(A4, INPUT);
    Serial.begin(9600);
    pinMode(A5, INPUT);
    Serial.begin(9600);

  for(j=8; j<14; j++){
    pinMode(j, OUTPUT);
  }
}
void loop()
{
  valor_carga1 = analogRead(A0);
  Serial.print (valor_carga1);
  Serial.print("\t");
  delay(10);

  valor_carga2 = analogRead(A1);
  Serial.print (valor_carga2);
  Serial.print("\t");
  delay(500);
  
  valor_carga3 = analogRead(A2);
  Serial.print (valor_carga3);
  Serial.print("\t");
  delay(500);

  valor_carga4 = analogRead(A3);
  Serial.print (valor_carga4);
  Serial.print("\t");
  delay(500);

  valor_carga5 = analogRead(A4);
  Serial.print (valor_carga5);
  Serial.print("\t");
  delay(500);

  valor_carga6 = analogRead(A5);
  Serial.println (valor_carga6);
  delay(500);

  if(valor_carga1>1000){
    digitalWrite(13, HIGH);
  }else{ 
    digitalWrite(13, LOW);
  }

  if(valor_carga2>1000){
    digitalWrite(12, HIGH);
  }else{ 
    digitalWrite(12, LOW);
  }

  if(valor_carga3>1000){
    digitalWrite(11, HIGH);
  }else{ 
    digitalWrite(11, LOW);
  }

  if(valor_carga4>1000){
    digitalWrite(10, HIGH);
  }else{ 
    digitalWrite(10, LOW);
  }

  if(valor_carga5>1000){
    digitalWrite(9, HIGH);
  }else{ 
    digitalWrite(9, LOW);
  }

  if(valor_carga6>1000){
    digitalWrite(8, HIGH);
  }else{ 
    digitalWrite(8, LOW);
  }
}


## Imagens

