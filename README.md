# Домашнее задание

public class JvmComprehension {
    // класс отдается для загрузки в систему загрузчиков классов, проходит процедура
    //связывания (Linking), где код проверяется на "валидность". Данные о классе отправляются в Metaspace


    public static void main(String[] args) {//В момент вызова метода создается фрейм(кадр) в стеке
        int i = 1;                      // Информация попадает в стек Stack Memory
        Object o = new Object();        // Информация попадает в heap (куча). По завершению метода printAll должен собраться сборщиком мусора
        Integer ii = 2;                 // Информация попадает в стек Stack Memory
        printAll(o, i, ii);             // В момент вызова создается фрейм в стеке. Stack Memory
        System.out.println("finished"); // Создается новый фрейм в стеке
    }

    private static void printAll(Object o, int i, Integer ii) {
        Integer uselessVar = 700;                   // Информация попадает в стек Stack Memory
        System.out.println(o.toString() + i + ii);  // Создается новый фрейм в стеке
    }
}