# Notes

## Unity

*   在 `TouchPhase.Begin` 触发后，如果手指未移动，那么 `TouchPhase.Stationary`
    将会触发。

*   使UI图片占满全屏的方法：

    1.  添加 `Image` component, 点击 `Set Native Size` 使得 `RectTransform`
        与图片的 大小一致。

    2.  添加 `AspectRatioFitter` component, 这时 `aspect ratio` 应与图片一致。

    3.  更改 `aspect mode` 至 `Envelop parent`.

## .NET

*   `KeyValuePair` 为只读。

*   使用 `Any()` 而不是 `Count() == 0` 来检测 `IEnumerable` 是否为空。

*   Covariance 与 contravariance 的区別.

        // 假设 A 为 covariance.
        // B 继承 A
        // 那么
        IFoo<B> y;
        IFoo<A> x = y;

        // 假设 A 为 is contravariance
        // B 继承 A
        // 那么
        IFoo<A> x;
        IFoo<B> y = x;
