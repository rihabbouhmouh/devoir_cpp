# devoir_cpp
[Atelier 3 rihab bouhmouch.pdf](https://github.com/user-attachments/files/17492876/Atelier.3.rihab.bouhmouch.pdf)

Atelier 3:
 #include <iostream>
 #include <string>
 using namespace std;
 class Voiture {
 private:
 string marque;
 string modele;
 int annee;
 float kilometrage;
 float vitesse;
 public:
 Voiture();
 Voiture(string ma, string mo, int a, float km, float v);
 void accelerer(float valeur);
 void freiner(float valeur) ;
 void afficherInfo() ;
 void avancer(float distance) ;
    ~Voiture() ;
 };
 Voiture::Voiture(): marque("unknown"), modele("unknown"), annee(0), kilometrage(0.0), 
vitesse(0.0){}
 Voiture::Voiture(string ma, string mo, int a, float km, float v) : marque(ma), modele(mo), annee(a), 
kilometrage(km), vitesse(v){}
 void Voiture:: accelerer(float valeur){
        vitesse+=valeur
    }
 void Voiture:: freiner(float valeur){
        vitesse-=valeur;
 if(vitesse<0){
            vitesse=0;
        }
    }
 void Voiture:: afficherInfo(){
 cout<<"marque: "<<marque<<endl;
 cout<<"Modèle: " << modele<<endl;
 cout<< "Année: " << annee <<endl;
 cout<<"Kilométrage: " << kilometrage<<" km"<<endl;
 cout << "Vitesse: " << vitesse << " km/h"<<endl;
    }
 void Voiture:: avancer(float distance){
 kilometrage+=distance;
    }
    Voiture::~Voiture(){
 cout<<"la voiture est detruite"<<endl;
    }
 int main() {
    Voiture v1;
 v1.afficherInfo();
 v1.accelerer(10.0);
 v1.avancer(80.0);
 v1.freiner(20.0);
 v1.afficherInfo();
    Voiture v2("BMW", "M1", 1981, 15000.5, 120.0);
 v2.afficherInfo();
 v2.accelerer(50.0);
 v2.avancer(100.0);
 v2.freiner(40.0);
 v2.afficherInfo();
 return 0;
 }
