# Algorithm_mokexam

## πTest1 : λͺ μκ° νλλΌ?
> κ²½μμ΄λ ν­ν΄μμ ν μ£Ό λμ κ³΅λΆ κΈ°λ‘μ λ¨κΈΈ μκ³ λ¦¬μ¦μ λ§λ€μ΄λ³΄κΈ°λ‘ κ²°μ¬νλ€.  
> ν­ν΄μ μ²΄ν¬μΈ νμ΄μ§μλ λͺκ°μ§ μ‘°κ±΄μ΄ μλλ° μ΄λ₯Ό λ§μ‘±νλ μκ³ λ¦¬μ¦μ λ§λ€μ΄λ³΄μ.  
>> μ²΄ν¬μΈκ³Ό μ²΄ν¬μμμ ν­μ μ μμ μ§νν κ²μΌλ‘ κ°μ νλ€.  
>> μ²΄ν¬μμμ ν  λ μ΅μΌ μκ°μ 24+a λ‘ κ³μ°νλ€. μ¦ μλ²½ 2μλ 24+2 μΈ 26μΌλ‘ νκΈ°νλ€.  
>> μ²΄ν¬μΈ νμ΄μ§λ μ²΄ν¬μμμ΄ μλ²½ 5μ μ κ°μ΄λ μλ²½ 5μλ₯Ό λμ΄κ°λ©΄ μ²΄ν¬μμμ κΉλΉ‘ν κ²μΌλ‘ κ°μ£Όνλ€.  
>> λ°λΌμ μλ²½ 5μκ° λμ΄κ° μ²΄ν¬μμμ νκ² λλ©΄ μλμΌλ‘ μ²΄ν¬μμμ μ€ν 9μ(21μ)λ‘ ν κ²μΌλ‘ μ²λ¦¬νλ€.  
>>> μ²΄ν¬μΈ(checkin)κ³Ό μ²΄ν¬μμ(checkout)μ μ§νν μκ°μ΄ λ΄κΈ΄ λ°°μ΄ λ κ°κ° μ£Όμ΄μ§λ€.  
>>> κ° λ°°μ΄μλ μμμΌλΆν° μΌμμΌκΉμ§ μ²΄ν¬μΈ/μμμ ν μκ°μ΄ λ΄κ²¨μλ€.  
>>>checkinκ³Ό checkout λ°°μ΄μ κΈΈμ΄λ κ°κ° 7 μ΄λ€.

<br>

```
public class Main {
    public int solution(int[] arr1, int[] arr2) {
        int answer = 0;
        return answer;
    }

    public static void main(String[] args) {
        Main method = new Main();
        int[] arr1 = {9, 9, 9, 9, 7, 9, 8};
        int[] arr2 = {23, 23, 30, 28, 30, 23, 23};
        System.out.println(method.solution(arr1, arr2));
    }
}
```
<br>

### β¨ λμ νμ΄ β¨
1. κΈ°λ³Έμ μΌλ‘ arr2[i] - arr1[i] λ₯Ό νλ©΄ νλ£¨λμμ κ³΅λΆμκ°μ΄ λμ¨λ€.
2. μ΄κ²μ 7λ² λ°λ³΅νλ©΄ μΌμ£ΌμΌ κ° μ΄ κ³΅λΆμκ°μ΄ λμ¨λ€.
3. λ€λ§, μλ²½ 5μκ° λμ΄κ°λ μκ°(arr2κ° 29μ΄μμΌ κ²½μ°)μ arr2λ₯Ό 21λ‘ μΉννλ€.

<br>

```
public class Main {
    public int solution(int[] arr1, int[] arr2) {
        int answer = 0;

        for(int i = 0; i < arr1.length; i++) {
        // arr2κ° 29μ΄μμΌ κ²½μ° 21 - arr1μ ν΄μ€λ€.
          if(arr2[i] >= 29) {
            answer += 21 - arr1[i];
        // κ·Έλ μ§ μμ κ²½μ°λ arr2μμ arr1μ κ°μ μΈλ±μ€λΌλ¦¬ λ§μ΄λμ€ν΄μ€λ€.
          } else {
            answer += arr2[i] - arr1[i];
          }
        }
      
        return answer;
    }

  
    public static void main(String[] args) {
        Main method = new Main();
        int[] arr1 = {9, 9, 9, 9, 7, 9, 8};
        int[] arr2 = {23, 23, 30, 28, 30, 23, 23};
        System.out.println(method.solution(arr1, arr2));
    }
}
```

<br>

#### μ‘°κ±΄λ€λ κΉλ€λ‘­μ§ μκ³  λ³λ€λ₯Έ μ΄λ €μ μμ΄ ν μ μμλ€!

<br>

## πTest2 : μ λλ₯ λ°κ²¬
> μμ§λ μ€λ ν­ν΄99λ₯Ό μμνλ€.  
> μ±κ²©μ΄ κΈν μμ§λ ν­ν΄ 1μΌ μ°¨λΆν° μΈμ  μλ£λ₯Ό νκ²λ  μ§ κΆκΈνλ€.  
> ν­ν΄ 1μΌ μ°¨ λ μ§λ₯Ό μλ ₯νλ©΄ 98μΌ μ΄ν ν­ν΄λ₯Ό μλ£νκ² λλ λ μ§λ₯Ό κ³μ°ν΄μ£Όλ μκ³ λ¦¬μ¦μ λ§λ€μ΄λ³΄μ.  
>> 1 β€ month β€ 12  
>> 1 β€ day β€ 31 (2μμ 28μΌλ‘ κ³ μ ν©λλ€, μ¦ μ€μΌμ κ³ λ €νμ§ μμ΅λλ€.)  

<br>

```
public class Main {
    public String solution(int month, int day) {
        String answer = "";
        return answer;
    }

    public static void main(String[] args) {
        Main method = new Main();
        System.out.println(method.solution(1, 18));
    }
}
```

<br>


### β¨ λμ νμ΄ β¨
```
int[] months = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12};
int[] date = {31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31};
```
1. μ°μ  monthsλΌλ 1~12μκΉμ§λ₯Ό μ μ΄λμ λ°°μ΄κ³Ό dateλΌλ κ° μμ μ΄ μΌμλ₯Ό μ μ λ°°μ΄ λ κ°μ§λ₯Ό μ μΈν΄λμλ€.
2. μ£Όμ΄μ§λ μΌμλ₯Ό 6μ 22μΌμ΄λΌκ³  κ°μ νλ€.  
3. μ£Όμ΄μ§ μΌ(22μΌ)μ 98μΌμ λνλ€. > 120μΌ  
4. 6μκ³Ό κ°μ μΈλ±μ€(5λ² μΈλ±μ€)μΈ date[5]μ valueλ₯Ό 120μΌμμ λ§μ΄λμ€νλ€. > 90μΌ
5. μΈλ±μ€λ₯Ό +1ν΄μ 7μμ μΌμλ₯Ό λ§μ΄λμ€νλ€. > 59μΌ
6. 8μμ μΌμλ₯Ό λ§μ΄λμ€νλ€. > 28μΌ
7. 9μμ μΌμλ‘ λ§μ΄λμ€ν  μ μμΌλ―λ‘ λ©μΆλ€.
8. 8μμ μΌμκΉμ§ λ§μ΄λμ€ νμΌλ―λ‘ μμ 9μμ΄ λκ³  μΌμ μ΅μ’μ μΌλ‘ λ¨μ 28μΌμ΄ λλ€.

<br>

```
public class Main {
    public String solution(int month, int day) {
        String answer = "";

        int[] months = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12};
        int[] date = {31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31};

        int days = day + 98;   // μ£Όμ΄μ§ μΌμ 98 λνκΈ°
        int idx = month - 1;   // μΈλ±μ€ λ³μ μ μΈ, μΈλ±μ€λ μ€μ  μμ -1μ΄λ―λ‘(1μμ΄λ©΄ 0λ² μΈλ±μ€μ΄λ―λ‘) -1μ ν΄μ€λ€.
        int mon = month;       // μΈλ±μ€κ° 1 λ³ννλ λ§νΌ μλ 1 λ³νλμ΄μΌ νλ―λ‘ λ°λ‘ λ³μλ₯Ό μ μΈν΄μ€λ€.
          
        while(days > date[idx]) {         // μΌμ 98 λν μκ° λ€μ dateμΈλ±μ€λ³΄λ€ ν° λμ μλλ₯Ό μννλ€.
          days -= date[idx];              // daysμ μ²μ μ£Όμ΄μ§ μμ μΈλ±μ€κ³Ό κ°μ date μΈλ±μ€μ valueλ₯Ό λ§μ΄λμ€ν΄μ€λ€.
          idx++;                          // κ·Έ νμ μΈλ±μ€λ₯Ό 1 μ¦κ°
          mon++;                          // κ·Έλ¦¬κ³  μλ 1 μ¦κ°
          if(idx == 12) {                 // λ§μ½μ idxκ° 12κ° λλ€λ©΄, μ΄ μΈλ±μ€μ κΈΈμ΄λ 11μ΄λ―λ‘(12μ λ€μμ 1μλ‘ λμ΄κ°λ μ‘°κ±΄)
           idx = 0;                       // μΈλ±μ€λ₯Ό 0μΌλ‘ μ΄κΈ°ννλ€.(1μμ μΈλ±μ€λ‘ λμ΄μ΄)
           mon = 1;                       // μμ 1μλ‘ μ΄κΈ°ννλ€.(12μμμ 1μλ‘ λμ΄μ΄)
          }
        } answer = mon+"μ "+days+"μΌ";
        
        return answer;
    }

  
    public static void main(String[] args) {
        Main method = new Main();
        System.out.println(method.solution(1, 18));
    }
}
```

<br>

#### μ΄λ»κ² νμ΄λκ°μΌ ν μ§ κ°μ λͺ»μ‘μλ λ¬Έμ μ΄λ€.  
#### μ΄λ¦¬μ λ¦¬ λν΄λ³΄κ³  νλ€κ° μ°μ°ν μ£Όμ΄μ§ μΌμ 98μ λνκ³   
#### κ·Έ νμ 30 λ°μΌλ‘ λ΄λ €κ° λκΉμ§ λΊλλ μμ μ μ λ΅κ³Ό κ°μ μΌμ΄ λμ€κΈΈλ   
#### λλ΅ μ΄λ°μμΌλ‘ μ κ·Όνλ©΄ λκ² κ΅¬λ νκ³  κΉ¨λ¬μλ€.  
#### λ¬Έμ λ₯Ό λ¨μνν΄μ(λ¨μν 30 λ°μΌλ‘ λ΄λ €κ° λκΉμ§ λΊλ€λκ°)  
#### μ κ·Όν νμ μ€μ λ‘ μ½λλ₯Ό μμ±νλ©΄μ κ΅¬μ²΄ννλ κ²μ΄ μ£Όμνλ κ² κ°λ€.  
#### μ κ·Όλ°©λ²μ μμλΈ νμ μ½λλ₯Ό μμ±νλ κ²μ λΉκ΅μ  μ¬μ κ³   
#### λ¨Έλ¦ΏμμΌλ‘ λͺ¨λ  κ²μ κ·Έλ¦° νμ μ½λ μμ±μ λ€μ΄κ°λ κ²μ΄ μλλΌ   
#### μ½λμμ±μ νλ©΄μ νμν λ³μλ₯Ό μΆκ°μ μΌλ‘ μ μΈνκ³  μ½λλ₯Ό μμ ν΄κ°λ©° μμ±μν¬ μ μμλ€.  
#### μ²μμλ idx λ³μλ μμκ³   
#### mon λ³μλ μμ΄ month μ κ·Έλλ‘ κ°μ μ μ₯νλ€λ³΄λ μ€λ₯κ° μμμΌλ μμ±νλ©΄μ μμ ν  μ μμλ€.  
#### λ¬λ ₯ λ¬Έμ λ μκ³ λ¦¬μ¦ μ°μ΅ν  λμλ νμ§ λͺ»νκ³  λλ €μ λ λ¬Έμ μΈλ°  
#### μ΄ λ¬Έμ λ₯Ό νλ©΄μ μμ κ°μ΄ μ‘°κΈ μκ²Όλ€κ³  ν  μ μκ² λ€.  
