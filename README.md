# 递归+高阶函数描述算法 (Clojure)

### 快速排序

```clojure
(def sort
  (fn [xs]
    (if (empty? xs)
      []
      (let [pivot (first xs)
            as (sort
                (filter
                 (fn [x]
                   (<= x pivot))
                 (rest xs)))
            bs (sort
                (filter
                 (fn [x]
                   (< pivot x))
                 (rest xs)))]
        (concat as [pivot] bs)))))

(sort [11 1 8 5 3]) ;; => (1 3 5 8 11)
```
### 二叉树

```clojure

```
