"""
    Elementwise Add Operator.
    Add two tensors element-wise
    The equation is:

    ..  math::

        Out=X+Y

    $X$ the tensor of any dimension.
    $Y$ the tensor whose dimensions must be less than or equal to the dimensions of $X$.

    This operator is used in the following cases:

    1. The shape of $Y$ is the same with $X$.
    2. The shape of $Y$ is a continuous subsequence of $X$.


        For example:

        .. code-block:: text

            shape(X) = (2, 3, 4, 5), shape(Y) = (,)
            shape(X) = (2, 3, 4, 5), shape(Y) = (5,)
            shape(X) = (2, 3, 4, 5), shape(Y) = (4, 5), with axis=-1(default) or axis=2
            shape(X) = (2, 3, 4, 5), shape(Y) = (3, 4), with axis=1
            shape(X) = (2, 3, 4, 5), shape(Y) = (2), with axis=0
            shape(X) = (2, 3, 4, 5), shape(Y) = (2, 1), with axis=0
