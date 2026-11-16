### 1. Where would you look first?

I would start with `naturaldelta` in `time.py`. It has the highest complexity score in the report: CC 35, rank E, and it is 164 lines long. The function has many branches for different time ranges and units, but it is not deeply nested throughout. It converts the input and chooses a readable, localized description. Those steps fit together, so the function seems cohesive even though it is long and branch-heavy.

### 2. Is the worst function really debt?

The highest-complexity function is `naturaldelta`, and its complexity appears to come largely from the number of cases it must handle: small durations, larger units, rounding, singular and plural wording, and invalid or non-finite inputs. That complexity may be justified by the function's behavior rather than being accidental. It has many branches, but it isn’t deeply nested throughout. Most cases are a sequence of checks for duration ranges and units. It handles input conversion and then chooses and formats a natural-language duration. Those are multiple steps, but they serve one cohesive purpose. The high complexity seems largely tied to supporting many duration cases, rather than obviously unrelated responsibilities.

### 3. Do the signals agree?

The report found no TODO, FIXME, or other tracked SATD comments in the scanned source, so there are no such comments to compare with the hotspots. It did find 15 duplicate patterns, with the listed examples in `number.py`. The largest complexity and length findings are in `time.py`, although `number.py` also contains the complex `metric` function. The signals therefore overlap only partly: `time.py` stands out for complexity and length, while `number.py` stands out for duplication.
