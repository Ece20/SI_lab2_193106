# SI_lab2_193106

## Цикломатска комплексност
цикломатската комплексност е 7 ,7 региони и p+1=6+1=7

### Control flow graph
![image](https://user-images.githubusercontent.com/80163148/119615264-80ca8c00-bdff-11eb-8b12-5d9a5ccd3d60.png)

#### Тест случаи
class SILab2Test {

    @Test
    void ConditionTest1() {
        Time time = new Time(-3, 6, 10);
        List<Time> timesList = new ArrayList<>();
        timesList.add(time);
        try {
            SILab2.function(timesList);
        } catch (Exception ex) {
            assertEquals(ex.getMessage(), "The hours are smaller than the minimum");
        }
    }


    @Test
    void ConditionTest2() {
        Time time = new Time(29, 17, 28);
        List<Time> timesList = new ArrayList<>();
        timesList.add(time);
        try {
            SILab2.function(timesList);
        } catch (Exception ex) {
            assertEquals(ex.getMessage(), "The hours are grater than the maximum");
        }
    }

    @Test
    void ConditionTest3() {
        Time time = new Time(14, -9, 24);
        List<Time> timesList = new ArrayList<>();
        timesList.add(time);
        try {
            SILab2.function(timesList);
        } catch (Exception ex) {
            assertEquals(ex.getMessage(), "The minutes are not valid!");
        }
    }

    @Test
    void ConditionTest4() {
        Time time = new Time(15, 69, 15);
        List<Time> timesList = new ArrayList<>();
        timesList.add(time);
        try {
            SILab2.function(timesList);
        } catch (Exception ex) {
            assertEquals(ex.getMessage(), "The minutes are not valid!");
        }
    }

    @Test
    void ConditionTest5() {
        Time time = new Time(22, 51, -10);
        List<Time> timesList = new ArrayList<>();
        timesList.add(time);
        try {
            SILab2.function(timesList);
        } catch (Exception ex) {
            assertEquals(ex.getMessage(), "The seconds are not valid");
        }
    }

    @Test
    void ConditionTest6() {
        Time time = new Time(16, 20, 80);
        List<Time> timesList = new ArrayList<>();
        timesList.add(time);
        try {
            SILab2.function(timesList);
        } catch (Exception ex) {
            assertEquals(ex.getMessage(), "The seconds are not valid");
        }
    }

    @Test
    void ConditonTest7() {
        Time time = new Time(15,12,10);
        List<Time> timesList = new ArrayList<>();
        List<Integer> result = new ArrayList<>();
        timesList.add(time);
        result = SILab2.function(timesList);
        assertEquals(result.get(0).intValue(),time.getHours()*3600 + time.getMinutes()*60 + time.getSeconds());
    }

    @Test
    void ConditionTest9() {
        Time time = new Time(24, 10, 0);
        List<Time> timesList = new ArrayList<>();
        timesList.add(time);
        try {
            SILab2.function(timesList);
        } catch (Exception ex) {
            assertEquals(ex.getMessage(), "The time is greater than the maximum");
        }
    }
    @Test
    void ConditonTest10() {
        Time time = new Time(24,0,0);
        List<Time> timesList = new ArrayList<>();
        List<Integer> result = new ArrayList<>();
        timesList.add(time);
        result = SILab2.function(timesList);
        assertEquals(result.get(0).intValue(),time.getHours()*3600 + time.getMinutes()*60 + time.getSeconds());
    }

    @Test
    void ConditionTest11() {
        Time time = new Time(24, 0, 10);
        List<Time> timesList = new ArrayList<>();
        timesList.add(time);
        try {
            SILab2.function(timesList);
        } catch (Exception ex) {
            assertEquals(ex.getMessage(), "The time is greater than the maximum");
        }
    }

Направени се тест случаи за сите ,најдени се вредности за да поминат тестовите -за да влезат и да го извршат делот .
