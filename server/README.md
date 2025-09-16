If you encounter SSL certificate validation errors when running the agent with the Tavily Search tool, you may need to update your certificates. This is a common issue that can occur when Python cannot locate or validate the necessary SSL certificates.

Run these 2 commands in your terminal: 

1. pip install certifi
2. /Applications/Python\ 3.9/Install\ Certificates.command

Docker commands

docker build -t sales-agent:latest .

docker run -d -p 8000:8000 \ 
   -e TAVILY_API_KEY=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
   -e GROQ_API_KEY=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  \
   --name sales-agent-container sales-agent:latest