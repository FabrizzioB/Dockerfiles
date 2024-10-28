# Use the official PostgreSQL image
FROM postgres:latest

# Set build-time arguments (can be overridden at build time)
ARG POSTGRES_USER=myuser
ARG POSTGRES_PASSWORD=mypassword
ARG POSTGRES_DB=mydatabase

# Set environment variables for PostgreSQL
# These can be overridden at runtime if needed
ENV POSTGRES_USER=${POSTGRES_USER}
ENV POSTGRES_PASSWORD=${POSTGRES_PASSWORD}
ENV POSTGRES_DB=${POSTGRES_DB}

# Create a volume for PostgreSQL data
VOLUME ["/var/lib/postgresql/data"]

# Expose the default PostgreSQL port
EXPOSE 5432

# Health check to verify that PostgreSQL is running
HEALTHCHECK CMD pg_isready -U ${POSTGRES_USER} || exit 1
