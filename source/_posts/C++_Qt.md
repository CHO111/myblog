---
title: C++ Qt
date: 2021-06-18 15:55:34
tags: C++, Qt
category: C++
---
# C++ Qt로 간단한 GUI만들기

![](https://user-images.githubusercontent.com/54093963/122520501-a178b100-d04e-11eb-9900-16dfb2c721c1.png)

사진과 같은 GUI를 구현 해보자!. 

프로젝트명은 QtWidgetsApplication1 로 생성하였다.

## UI 구성
![](https://user-images.githubusercontent.com/54093963/122521545-e8b37180-d04f-11eb-9a3b-d92118f2d89e.PNG)
![](https://user-images.githubusercontent.com/54093963/122521552-ec46f880-d04f-11eb-88c7-2d538d7baf62.PNG)


## h.파일코드
```C++
#pragma once

#include <QtWidgets/QDialog>
#include "ui_QtWidgetsApplication1.h"

class QtWidgetsApplication1 : public QDialog
{
    Q_OBJECT

public:
    QtWidgetsApplication1(QWidget *parent = Q_NULLPTR);

private:
    Ui::QtWidgetsApplication1Class ui;

public slots:
    void btn_run_clicked();
};
```

## cpp.파일코드
```C++
#include "QtWidgetsApplication1.h"

QtWidgetsApplication1::QtWidgetsApplication1(QWidget *parent)
    : QDialog(parent)
{
    ui.setupUi(this);
    connect(ui.btn_run, SIGNAL(clicked()), this, SLOT(btn_run_clicked()));
    connect(ui.checkBox_1, SIGNAL(clicked()), this, SLOT(checkBox1_clicked()));
    connect(ui.checkBox_2, SIGNAL(clicked()), this, SLOT(checkBox2_clicked()));
    connect(ui.checkBox_3, SIGNAL(clicked()), this, SLOT(checkBox3_clicked()));
    connect(ui.checkBox_4, SIGNAL(clicked()), this, SLOT(checkBox3_clicked()));

    ui.comboBox->addItem("Male");
    ui.comboBox->addItem("FeMale");

}

void QtWidgetsApplication1::btn_run_clicked()
{
    ui.label_6->setText("Age:" + ui.spinBox->cleanText());

    ui.label_5->setText("Gender:" + ui.comboBox->currentText());
    
    QString chk1 = "", chk2 = "", chk3 = "", chk4="";
    if (ui.checkBox_1->isChecked())
        chk1 = "Hobby :Watching Movie";
    if (ui.checkBox_2->isChecked())
        chk2 = "Hobby :Sports";
    if (ui.checkBox_3->isChecked())
        chk3 = "Hobby :Drawing";
    if (ui.checkBox_4->isChecked())
        chk3 = "Hobby :Pet";
    ui.label_4->setText(QString("\n%1 \n%2 \n%3 \n%4").arg(chk1, chk2, chk3, chk4));
};
```

## 실행결과

![](https://user-images.githubusercontent.com/54093963/122522076-8444e200-d050-11eb-8139-7c611f88cbb3.PNG)
