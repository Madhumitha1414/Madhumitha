from flask import Flask, request, jsonify
import random
import difflib

app = Flask(__name__)

# (Reuse RECIPES and helper functions from above: suggest_random_recipe, find_recipes_by_ingredients, fuzzy_search_recipe, format_recipe)

@app.route("/ask", methods=["GET"])
def ask():
    q = request.args.get("q", "")
    if not q:
        return jsonify({"error": "Query parameter 'q' is required."}), 400
    answer = handle_question(q)
    return jsonify({"question": q, "answer": answer})

if __name__ == "__main__":
    app.run(debug=True)
