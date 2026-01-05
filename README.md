## Hi👋 
### Welcome to my GitHub Profile

```python
import json

from typing import List, Dict
from pydantic import BaseModel, Field


class Skills(BaseModel):
    objective: str = "Aspiring machine learning engineer, trying to change the world one line of code at a time"
    languages: List[str] = ["Python", "Swift", "Go", "TypeScript"]
    frameworks: List[str] = ["PyTorch", "FastAPI", "SwiftUI", "UIKit"]
    libraries: Dict[str, List[str]] = {
        "ML": ["PyTorch Geometric", "TensorFlow", "NumPy", "Pandas", "Scikit-Learn"],
        "Frontend": ["React", "Vue"]
    }
    databases: List[str] = ["GraphQL", "SQLite", "NoSQL"]
    
    def jsonify(self) -> str:
        return json.dumps(self.model_dump(), indent=4)


skills = Skills()
print(skills.jsonify())
```

Some work examples: [Projects](Projects.md)
