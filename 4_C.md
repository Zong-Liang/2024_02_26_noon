1. ```c
   #include <stdio.h>
   
   int main() {
       int a[3][4];
       int positive_count = 0, negative_count = 0, zero_count = 0;
   
       // 从键盘输入矩阵元素
       printf("请输入3*4整数矩阵的元素：\n");
       for (int i = 0; i < 3; i++) {
           for (int j = 0; j < 4; j++) {
               scanf("%d", &a[i][j]);
           }
       }
   
       // 统计正数、负数和0的个数
       for (int j = 0; j < 4; j++) {
           for (int i = 0; i < 3; i++) {
               if (a[i][j] > 0)
                   positive_count++;
               else if (a[i][j] < 0)
                   negative_count++;
               else
                   zero_count++;
           }
       }
   
       // 输出统计结果
       printf("正数个数：%d\n", positive_count);
       printf("负数个数：%d\n", negative_count);
       printf("0的个数：%d\n", zero_count);
   
       return 0;
   }
   ```

2. ```c
   #include <stdio.h>
   
   // 函数声明
   int Sum(int num);
   
   int main() {
       int number, sum;
   
       // 从键盘输入整数
       printf("请输入一个整数：");
       scanf("%d", &number);
   
       // 调用函数计算每一位数字之和
       sum = Sum(number);
   
       // 输出结果
       printf("每一位数字之和为：%d\n", sum);
   
       return 0;
   }
   
   // 统计每一位数字之和的函数
   int Sum(int num) {
       int sum = 0;
   
       // 循环累加数字的每一位
       while (num != 0) {
           sum += num % 10; // 求余数得到最后一位数字，并加到sum中
           num /= 10; // 将num除以10，去掉最后一位数字
       }
   
       return sum;
   }
   ```

3. ```c
   #include <stdio.h>
   
   int main() {
       int x, y;
   
       // 假设先让y=-1
       y = -1;
   
       // 输入x的值
       printf("请输入一个整数x：");
       scanf("%d", &x);
   
       // 根据x的值更新y的值
       if (x > 0){
           y = 1;
       }
       else if (x == 0){
           y = 0;
       }
       else{
           y=-1;
       } 
   
       // 输出y的值
       printf("根据条件更新后，y的值为：%d\n", y);
   
       return 0;
   }
   
   ```

4. ```c
   #include <stdio.h>
   
   // 函数声明
   void Join(char str1[], char str2[]);
   
   int main() {
       char str1[80], str2[40];
   
       // 从键盘输入两个字符串
       printf("请输入第一个字符串：");
       scanf("%s", str1);
       printf("请输入第二个字符串：");
       scanf("%s", str2);
   
       // 调用函数将两个字符串连接起来
       Join(str1, str2);
   
       // 输出结果
       printf("连接后的字符串：%s\n", str1);
   
       return 0;
   }
   
   // 将两个字符串连接为一个字符串的函数
   void Join(char str1[], char str2[]) {
       int i = 0, j = 0;
   
       // 找到str1的末尾
       while (str1[i] != '\0') {
           i++;
       }
   
       // 将str2的内容复制到str1的末尾
       while (str2[j] != '\0') {
           str1[i] = str2[j];
           i++;
           j++;
       }
   
       // 在连接后的字符串末尾添加字符串结束符 '\0'
       str1[i] = '\0';
   }
   ```