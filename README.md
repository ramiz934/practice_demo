# practice_demo
This is for practice
class Main {
    public static void main(String[] args) {
        String str= "java programming is a good programming java";
   Map.Entry<String,Long> s= Arrays.stream(str.split(""))
.collect(Collectors.groupingBy(Function.identity(),LinkedHashMap::new,Collectors.counting()))
        .entrySet().stream().filter(x->x.getValue()>1).findFirst().get();
        
        System.out.println(s);
    }
}
