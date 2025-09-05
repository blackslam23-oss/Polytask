from typing import List
import math

class Shape:
    """Base class for all shapes."""
    def draw(self) -> None:
        raise NotImplementedError("Draw method not implemented.")

    def area(self) -> float:
        raise NotImplementedError("Area method not implemented.")

    def __str__(self) -> str:
        return self.__class__.__name__

class Circle(Shape):
    def __init__(self, radius: float):
        self.radius = radius

    def draw(self) -> None:
        print(f"Drawing a Circle with radius {self.radius}")

    def area(self) -> float:
        return math.pi * self.radius ** 2

class Rectangle(Shape):
    def __init__(self, width: float, height: float):
        self.width = width
        self.height = height

    def draw(self) -> None:
        print(f"Drawing a Rectangle of width {self.width} and height {self.height}")

    def area(self) -> float:
        return self.width * self.height

class Triangle(Shape):
    def __init__(self, base: float, height: float):
        self.base = base
        self.height = height

    def draw(self) -> None:
        print(f"Drawing a Triangle with base {self.base} and height {self.height}")

    def area(self) -> float:
        return 0.5 * self.base * self.height

class Canvas:
    """A canvas that can hold and draw multiple shapes."""
    def __init__(self):
        self.shapes: List[Shape] = []

    def add_shape(self, shape: Shape) -> None:
        self.shapes.append(shape)

    def draw_all(self) -> None:
        for shape in self.shapes:
            shape.draw()
            print(f"Area: {shape.area():.2f}\n")

# Example Usage
if __name__ == "__main__":
    canvas = Canvas()
    canvas.add_shape(Circle(radius=5))
    canvas.add_shape(Rectangle(width=3, height=4))
    canvas.add_shape(Triangle(base=6, height=2))

    canvas.draw_all()
