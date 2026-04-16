# User Isolation Tests

## Overview
One of the most important requirements in this project was to verify whether multiple users could work in the same environment without accessing or interfering with each other’s resources.

## Test Goal
The goal of the isolation testing was to evaluate whether the platform can support a shared ICT learning environment safely.

## Test Scenario
Two separate users were created in the environment.

Each user:
- had their own access
- created their own project or resources
- worked with their own virtual machines

The purpose was to verify that one user could not access or manage the resources of another user.

## What Was Evaluated
The testing focused on:
- visibility of virtual machines
- visibility of storage and network resources
- access rights between users
- separation of user-owned resources
- role-based restrictions

## Observations
The environment supported user separation well.

Key observations:
- users were limited to their own resources
- unauthorized access to another user’s environment was not possible
- role and access control behavior supported safe multi-user usage
- the platform structure was suitable for shared educational use

## Practical Importance
User isolation is critical in environments where multiple learners share the same infrastructure.

This is important for:
- educational labs
- practical training environments
- shared test platforms
- infrastructure learning scenarios

## Conclusion
The isolation testing showed that the environment can support multiple users in a controlled way.

This makes the platform suitable for learning environments where safe separation between users is required.
