import tkinter as tk
from tkinter import ttk

class UnitConverter:
    def __init__(self):
        self.root = tk.Tk()
        self.root.title("Unit Converter")
           
        self.label_input = ttk.Label(self.root, text="Enter value:")
        self.label_input.grid(row=0, column=0, padx=10, pady=10)

        self.entry_input = ttk.Entry(self.root, width=15)
        self.entry_input.grid(row=0, column=1, padx=10, pady=10)

        self.label_result = ttk.Label(self.root, text="Converted value:")
        self.label_result.grid(row=1, column=0, padx=10, pady=10)

        self.label_output = ttk.Label(self.root, text="")
        self.label_output.grid(row=1, column=1, padx=10, pady=10)

        self.unit_options = ['Meters', 'Kilometers', 'Centimeters', 'Millimeters',
                             'Feet', 'Inches', 'Yards', 'Miles', 'Nautical Miles']
        self.from_unit = ttk.Combobox(self.root, values=self.unit_options, width=12)
        self.from_unit.grid(row=0, column=2, padx=10, pady=10)
        self.from_unit.current(0)

        self.to_unit = ttk.Combobox(self.root, values=self.unit_options, width=12)
        self.to_unit.grid(row=1, column=2, padx=10, pady=10)
        self.to_unit.current(1)

        self.convert_button = ttk.Button(self.root, text="Convert", command=self.convert_units)
        self.convert_button.grid(row=2, column=1, padx=10, pady=10)

    def convert_units(self):
        try:
            value = float(self.entry_input.get())
            from_unit = self.from_unit.get()
            to_unit = self.to_unit.get()

            result = self.perform_conversion(value, from_unit, to_unit)

            self.label_output.config(text=f"{result:.4f} {to_unit}")

        except ValueError:
            self.label_output.config(text="Error: Invalid input")

    def perform_conversion(self, value, from_unit, to_unit):
        conversion_factors = {
            'Meters to Kilometers': 0.001,
            'Meters to Centimeters': 100,
            'Meters to Millimeters': 1000,
            'Meters to Feet': 3.28084,
            'Meters to Inches': 39.3701,
            'Meters to Yards': 1.09361,
            'Meters to Miles': 0.000621371,
            'Meters to Nautical Miles': 0.000539957,

            'Kilometers to Meters': 1000,
            'Kilometers to Centimeters': 100000,
            'Kilometers to Millimeters': 1000000,
            'Kilometers to Feet': 3280.84,
            'Kilometers to Inches': 39370.1,
            'Kilometers to Yards': 1093.61,
            'Kilometers to Miles': 0.621371,
            'Kilometers to Nautical Miles': 0.539957,

            'Centimeters to Meters': 0.01,
            'Centimeters to Kilometers': 0.00001,
            'Centimeters to Millimeters': 10,
            'Centimeters to Feet': 0.0328084,
            'Centimeters to Inches': 0.393701,
            'Centimeters to Yards': 0.0109361,
            'Centimeters to Miles': 0.00000621371,
            'Centimeters to Nautical Miles': 0.00000539957,

            'Millimeters to Meters': 0.001,
            'Millimeters to Kilometers': 0.000001,
            'Millimeters to Centimeters': 0.1,
            'Millimeters to Feet': 0.00328084,
            'Millimeters to Inches': 0.0393701,
            'Millimeters to Yards': 0.00109361,
            'Millimeters to Miles': 0.000000621371,
            'Millimeters to Nautical Miles': 0.000000539957,

            'Feet to Meters': 0.3048,
            'Feet to Kilometers': 0.0003048,
            'Feet to Centimeters': 30.48,
            'Feet to Millimeters': 304.8,
            'Feet to Inches': 12,
            'Feet to Yards': 0.333333,
            'Feet to Miles': 0.000189394,
            'Feet to Nautical Miles': 0.000164579,

            'Inches to Meters': 0.0254,
            'Inches to Kilometers': 0.0000254,
            'Inches to Centimeters': 2.54,
            'Inches to Millimeters': 25.4,
            'Inches to Feet': 0.0833333,
            'Inches to Yards': 0.0277778,
            'Inches to Miles': 0.0000157828,
            'Inches to Nautical Miles': 0.0000137149,

            'Yards to Meters': 0.9144,
            'Yards to Kilometers': 0.0009144,
            'Yards to Centimeters': 91.44,
            'Yards to Millimeters': 914.4,
            'Yards to Feet': 3,
            'Yards to Inches': 36,
            'Yards to Miles': 0.000568182,
            'Yards to Nautical Miles': 0.000493737,

            'Miles to Meters': 1609.34,
            'Miles to Kilometers': 1.60934,
            'Miles to Centimeters': 160934,
            'Miles to Millimeters': 1609340,
            'Miles to Feet': 5280,
            'Miles to Inches': 63360,
            'Miles to Yards': 1760,
            'Miles to Nautical Miles': 0.868976,

            'Nautical Miles to Meters': 1852,
            'Nautical Miles to Kilometers': 1.852,
            'Nautical Miles to Centimeters': 185200,
            'Nautical Miles to Millimeters': 1852000,
            'Nautical Miles to Feet': 6076.12,
            'Nautical Miles to Inches': 72913.4,
            'Nautical Miles to Yards': 2025.37,
            'Nautical Miles to Miles': 1.15078,
        }

        conversion_key = f"{from_unit} to {to_unit}"
        reverse_conversion_key = f"{to_unit} to {from_unit}"

        if conversion_key in conversion_factors:
            factor = conversion_factors[conversion_key]
            converted_value = value * factor
            return converted_value
        elif reverse_conversion_key in conversion_factors:
            factor = conversion_factors[reverse_conversion_key]
            converted_value = value / factor
            return converted_value
        else:
            return "Conversion not supported"

    
        self.root.mainloop()

UnitConverter()


