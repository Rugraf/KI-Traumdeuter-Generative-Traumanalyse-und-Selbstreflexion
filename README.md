# KI-Traumdeuter-Generative-Traumanalyse-und-Selbstreflexion
KI-Traumdeuter verwendet generative KI und Sprachmodelle, um Träume zu analysieren und zu interpretieren, und bietet Nutzern Einblicke in ihr Unterbewusstsein und Anregungen zur Selbstreflexion.
import random

def analyze_dream(dream_description):
    """
    Simulates dream analysis by generating insights based on keywords.
    In a real application, this could be replaced with an AI model for more depth.
    """
    insights = {
        "flying": "Flying in dreams often symbolizes a desire for freedom or escape from current pressures.",
        "falling": "Falling can indicate anxiety and loss of control in your waking life.",
        "water": "Water often represents emotions and your unconscious mind.",
        "chasing": "Being chased in a dream might signify avoidance of a situation in waking life."
    }
    
    analysis = {"insights": [], "reflection_questions": []}
    for keyword, insight in insights.items():
        if keyword in dream_description.lower():
            analysis["insights"].append(insight)
            analysis["reflection_questions"].append(f"How does the theme of {keyword} relate to your current life situations?")
    
    if not analysis["insights"]:
        # Default message if no keywords match
        analysis["insights"].append("This dream seems unique. Reflect on what it means to you personally.")
        analysis["reflection_questions"].append("What feelings or thoughts does this dream bring up for you?")
    
    return analysis

def main():
    print("Welcome to KI-Traumdeuter: Generative Traumanalyse und Selbstreflexion")
    dream_description = input("Please describe your dream in a few sentences: ")
    
    analysis = analyze_dream(dream_description)
    
    print("\nDream Analysis:")
    for insight in analysis["insights"]:
        print(f"- {insight}")
        
    print("\nReflection Questions:")
    for question in analysis["reflection_questions"]:
        print(f"- {question}")

if __name__ == "__main__":
    main()
