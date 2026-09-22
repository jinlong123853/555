
#include <bits/stdc++.h>
using namespace std;
class Book {
private:
    string id;          // 书号
    string title;       // 书名
    string author;      // 作者
    string publisher;   // 出版社
    bool isBorrowed;    // 是否被借出

public:
    Book(string _id, string _title, string _author, string _pub) 
        : id(_id), title(_title), author(_author), publisher(_pub), isBorrowed(false) {}
    ~Book() {}
    string getId() const { return id; }
    string getTitle() const { return title; }
    bool getStatus() const { return isBorrowed; }
    
    void setBorrowed(bool status) { isBorrowed = status; }

    void display() const {
        cout << "书号:" << id << " | 书名:" << title << " | 作者:" << author 
             << " | 出版社:" << publisher << " | 状态:" << (isBorrowed ? "已借出" : "在馆") << endl;
    }
};

class User {
private:
    string id;      // 学号或工号
    string name;    // 姓名
    string password;// 密码

public:
    User(string _id, string _name, string _pwd) 
        : id(_id), name(_name), password(_pwd) {}

    string getId() const { return id; }
    string getName() const { return name; }
    string getPassword() const { return password; }

    void displayInfo() const {
        cout << "账号:" << id << " | 姓名:" << name << endl;
    }
};
