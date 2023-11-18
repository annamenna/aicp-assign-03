# aicp-assign-03
#include <iostream>
using namespace std;

// Source data matrix
int electricity_matrix[3][5] = {
    {90, 120, 180, 250, 310},
    {150, 170, 220, 280, 350},
    {210, 250, 320, 380, 450}
};

// Student ID
const char* student_id = "YourStudentID";

// Function to calculate and display cost for slab 1
void costSlab1() {
    int unit_range_min = 0;
    int unit_range_max = 100;
    int unit_cost = 10;

    int total_units = 0;
    for (int i = 0; i < 5; ++i) {
        total_units += electricity_matrix[0][i];
    }

    int total_cost = total_units * unit_cost;

    cout << "\nSlab 1 Bill:" << endl;
    cout << "Unit Range: " << unit_range_min << " - " << unit_range_max << endl;
    cout << "Total Units Consumed: " << total_units << endl;
    cout << "Unit Cost: Rs." << unit_cost << endl;
    cout << "Total Cost: Rs." << total_cost << endl;
}

// Function to calculate and display cost for slab 2
void costSlab2() {
    int unit_range_min = 101;
    int unit_range_max = 200;
    int unit_cost = 15;

    int total_units = 0;
    for (int i = 0; i < 5; ++i) {
        total_units += electricity_matrix[1][i];
    }

    int total_cost = total_units * unit_cost;

    cout << "\nSlab 2 Bill:" << endl;
    cout << "Unit Range: " << unit_range_min << " - " << unit_range_max << endl;
    cout << "Total Units Consumed: " << total_units << endl;
    cout << "Unit Cost: Rs." << unit_cost << endl;
    cout << "Total Cost: Rs." << total_cost << endl;
}

// Function to calculate and display cost for slab 3
void costSlab3() {
    int unit_range_min = 201;
    int unit_range_max = 300;
    int unit_cost = 20;

    int total_units = 0;
    for (int i = 0; i < 5; ++i) {
        total_units += electricity_matrix[2][i];
    }

    int total_cost = total_units * unit_cost;

    cout << "\nSlab 3 Bill:" << endl;
    cout << "Unit Range: " << unit_range_min << " - " << unit_range_max << endl;
    cout << "Total Units Consumed: " << total_units << endl;
    cout << "Unit Cost: Rs." << unit_cost << endl;
    cout << "Total Cost: Rs." << total_cost << endl;
}

// Main menu
int main() {
    char choice;

    do {
        cout << "\nStudent ID: " << student_id << endl;
        cout << "1. Display bill of slab 1 and slab 2" << endl;
        cout << "2. Display bill of slab 3" << endl;
        cout << "Any other key to exit" << endl;

        cout << "Enter your choice: ";
        cin >> choice;

        switch (choice) {
            case '1':
                costSlab1();
                costSlab2();
                break;
            case '2':
                costSlab3();
                break;
            default:
                cout << "Exiting the program." << endl;
                break;
        }

    } while (choice == '1' || choice == '2');

    return 0;
}
