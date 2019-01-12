---
layout: post
title:  "Welcome to windcat's blog!"
date:   2019-01-12 19:17:18 +0800
categories: java
---

{% highlight java %}

import java.util.Arrays;

/**
 * 这是给傻宝宝做练习题用的
 *
 * @author windcat
 */
public class SweetJavaStudy {

    /**
     * 找出整型k在array中的下标，如果k不在array中，则返回-1
     * 条件array中的元素已进行升序排序
     *
     * @param array 升序排序后的数组
     * @param k     整型数字
     * @return k在array的下标
     */
    public static int indexOf(int[] array, int k) {

        /*
         * TODO 在这里写
         */

        return -1;
    }

    /**
     * 找出array中的最大值
     *
     * @param array 无序数组
     * @return array中的最大值
     */
    public static int max(int[] array) {

        /*
         * TODO 在这里写
         */

        return Integer.MIN_VALUE;
    }

    /**
     * 计算array的平均值
     *
     * @param array 数组
     * @return array的平均值
     */
    public static double avg(double[] array) {
        /*
         * TODO 在这里写
         */

        return Double.MIN_VALUE;
    }

    /**
     * 颠倒数组中元素的顺序
     *
     * @param array 数组
     */
    public static void reverse(int[] array) {
        /*
         * TODO 在这里写
         */
    }

    /**
     * 判断数字n是否是素数
     *
     * @param n 整数
     * @return 是否是素数
     */
    public static boolean isPrime(int n) {
        return false;
    }


    public static void main(String[] args) {

        System.out.println("# 开始验证【indexOf】是否正确...");

        int[] array = {1, 3, 5, 7, 9};
        int k = 7;
        boolean result = SweetJavaStudy.indexOf(array, k) == 3;

        if (result) {
            System.out.println("$ 恭喜你【indexOf】做对了.");
        } else {
            System.err.println("**【indexOf】做错了.");
        }


        System.out.println("# 开始验证【max】是否正确...");

        result = SweetJavaStudy.max(array) == 9;

        if (result) {
            System.out.println("$ 恭喜你【max】做对了.");
        } else {
            System.err.println("**【max】做错了.");
        }


        System.out.println("# 开始验证【avg】是否正确...");

        double[] doubles = {1.1, 1.2, 1.3, 1.4, 1.5};

        result = Math.abs(SweetJavaStudy.avg(doubles) - 1.3) < 1e-6;

        if (result) {
            System.out.println("$ 恭喜你【avg】做对了.");
        } else {
            System.err.println("**【avg】做错了.");
        }

        System.out.println("# 开始验证【reverse】是否正确...");
        SweetJavaStudy.reverse(array);
        result = "[9, 7, 5, 3, 1]".equals(Arrays.toString(array));

        if (result) {
            System.out.println("$ 恭喜你【reverse】做对了.");
        } else {
            System.err.println("**【reverse】做错了.");
        }

        System.out.println("# 开始验证【isPrime】是否正确...");

        if (SweetJavaStudy.isPrime(3)) {
            System.out.println("$ 恭喜你【isPrime】做对了.");
        } else {
            System.err.println("**【isPrime】做错了.");
        }

    }
}

{% endhighlight %}
