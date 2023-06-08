#include <iostream>
#include <iomanip>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
    int lotteryNumber;

    cout << "*******************************************" << endl;
    cout << "   UCR MEDICAL RESIDENCY LOTTERY PROGRAM" << endl;
    cout << "*******************************************" << endl;


    cout << "\nSelect your desired medical specialization:" << endl;
    cout << "1. Cardiology" << endl;
    cout << "2. Dermatology" << endl;
    cout << "3. Neurology" << endl;
    cout << "4. Orthopedics" << endl;
    cout << "5. Pediatrics" << endl;


    string specialization;
    cin >> specialization;


    cout << "\nSelect your preferred language of communication:" << endl;
    cout << "1. English" << endl;
    cout << "2. Spanish" << endl;
    cout << "3. French" << endl;
    cout << "4. Arabic" << endl;
    cout << "5. Mandarin" << endl;


    string language;
    cin >> language;

    // Country preference
    cout << "\nSelect your preferred country for medical residency:" << endl;
    cout << "1. United States (English)" << endl;
    cout << "2. United Kingdom (English)" << endl;
    cout << "3. Canada (English, French)" << endl;
    cout << "4. Spain (Spanish)" << endl;
    cout << "5. France (French)" << endl;
    cout << "6. Saudi Arabia (Arabic)" << endl;
    cout << "7. China (Mandarin)" << endl;
    cout << "8. Venezuela (Spanish)" << endl;
    cout << "9. Colombia (Spanish)" << endl;
    cout << "10. Mexico (Spanish)" << endl;
    cout << "11. Nicaragua (Spanish)" << endl;


    string country;
    cin >> country;

    // Generate lottery number
    srand(time(0));
    lotteryNumber = rand() % 100 + 1;

    // Check lottery number against probabilities
    cout << "\nLottery Result:" << endl;

    if (lotteryNumber <= 70) {
        cout << "Congratulations! You have secured your preferred country." << endl;
        if (lotteryNumber <= 40) {
            cout << "You have also obtained your desired specialization." << endl;
        }
        else {
            cout << "However, you did not obtain your desired specialization." << endl;
        }
    }
    else {
        // Introduce a 3% chance of matching
        if (lotteryNumber <= 73) {
            cout << "Congratulations! You have secured your preferred country." << endl;
            if (lotteryNumber <= 43) {
                cout << "You have also obtained your desired specialization." << endl;
            }
            else {
                cout << "However, you did not obtain your desired specialization." << endl;
            }
        }
        else {
            cout << "Unfortunately, you did not secure your preferred country and specialization." << endl;
        }
    }

    // Display lottery number and probabilities
    cout << "\nLottery Information:" << endl;
    cout << "Your lottery number: " << lotteryNumber << endl;


    float countryProbability, specializationProbability;
    float languageFluencyWeight = 0.0;
    float countryLanguageMatchWeight = 0.0;

    if (language == "1") { // English fluency
        countryProbability = 75.0 / 100.0;
        specializationProbability = 45.0 / 100.0;
        languageFluencyWeight = 1.0;

        if (country == "1" || country == "2" || country == "3") {
            countryLanguageMatchWeight = 1.2; // Increased weight for English-speaking countries
        }
    }
    else if (language == "2") { // Spanish fluency
        countryProbability = 70.0 / 100.0;
        specializationProbability = 40.0 / 100.0;
        languageFluencyWeight = 1.0;

        if (country == "4" || country == "8" || country == "9" || country == "10" || country == "11") {
            countryLanguageMatchWeight = 1.2; // Increased weight for Spanish-speaking countries
        }
    }
    else if (language == "3") { // French fluency
        countryProbability = 70.0 / 100.0;
        specializationProbability = 40.0 / 100.0;
        languageFluencyWeight = 1.0;

        if (country == "3" || country == "5") {
            countryLanguageMatchWeight = 1.2; // Increased weight for French-speaking countries
        }
    }
    else if (language == "4") { // Arabic fluency
        countryProbability = 75.0 / 100.0;
        specializationProbability = 45.0 / 100.0;
        languageFluencyWeight = 1.0;

        if (country == "6") {
            countryLanguageMatchWeight = 1.2; // Increased weight for Arabic-speaking countries
        }
    }
    else if (language == "5") { // Mandarin fluency
        countryProbability = 65.0 / 100.0;
        specializationProbability = 35.0 / 100.0;
        languageFluencyWeight = 1.0;

        if (country == "7") {
            countryLanguageMatchWeight = 1.2; // Increased weight for Mandarin-speaking countries
        }
    }



    // Apply language fluency weight and country language match weight
    countryProbability *= languageFluencyWeight;
    countryProbability *= countryLanguageMatchWeight;

    cout << fixed << setprecision(2);
    cout << "Probability of securing your preferred country: " << countryProbability * 100 << "%" << endl;
    cout << "Probability of securing your desired specialization: " << specializationProbability * 100 << "%" << endl;

    // Display additional information based on language selection
    if (language == "1") {
        cout << "\nEnglish is widely spoken in medical institutions around the world." << endl;
    }
    else if (language == "2") {
        cout << "\nSpanish is spoken in medical institutions in Latin America and Spain." << endl;
    }
    else if (language == "3") {
        cout << "\nFrench is spoken in medical institutions in France and some African countries." << endl;
    }
    else if (language == "4") {
        cout << "\nArabic is spoken in medical institutions in the Middle East." << endl;
    }
    else if (language == "5") {
        cout << "\nMandarin is spoken in medical institutions in China and some Asian countries." << endl;
    }



    if (specialization == "1") {
        cout << "\nCardiology focuses on the diagnosis and treatment of heart-related diseases." << endl;
    }
    else if (specialization == "2") {
        cout << "\nDermatology deals with the diagnosis and treatment of skin-related conditions." << endl;
    }
    else if (specialization == "3") {
        cout << "\nNeurology specializes in the diagnosis and treatment of disorders of the nervous system." << endl;
    }
    else if (specialization == "4") {
        cout << "\nOrthopedics focuses on the diagnosis and treatment of musculoskeletal disorders and injuries." << endl;
    }
    else if (specialization == "5") {
        cout << "\nPediatrics deals with the medical care of infants, children, and adolescents." << endl;
    }

    cout << "\nThank you for participating in the Medical Residency Lottery Program!" << endl;

    return 0;
}
