package com.company;

import java.util.Scanner;

public class Main
{
    public static Person [] p = new Person[3];
    public static void main(String[] args)
    {
        func1();
        for(int i = 0; i < 3; i++)
        {
            p[i].print();
        }
    }

    public static void func1()
    {

        for(int i = 0; i < 3; i++)
        {
            Scanner input = new Scanner(System.in);
            System.out.println("ENTER PERSON DATA");
            String name = input.nextLine();
            String second_name = input.nextLine();
            int age = input.nextInt();
            System.out.println("DATA ENTERD");
            p[i] = new Person(name, second_name, age);
        }
    }
}

class Person
{
    String name;
    String second_name;
    int age;

    public  Person(String name1, String second_name1, int age1)
    {
        name = name1;
        second_name = second_name1;
        age = age1;
    }

    public void print()
    {
        System.out.println("PERSON DATA{name: " + name +"; second name: "+ second_name +"; age:" + age +"}");
    }
}
