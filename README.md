#include <iostream>
using namespace std;
class employee {
private:
    char name[20];
    int age;
    int salary;
public:
    void info() {
        cout << "\n Enter the employee name: ";
        cin >> name;
        cout << "\n Enter the employee age: ";
        cin >> age;
        cout << "\n Enter the employee salary: ";
        cin >> salary;
    }
  friend void display(const employee&);
};
void display(const employee& emp) {
    cout << "\n Employee Data: " << emp.name << "\t" << emp.age << "\t" << emp.salary;
}
int main() {
    employee person;
    person.info();
    display(person);
    return 0;
}# Manager-data-analysis
